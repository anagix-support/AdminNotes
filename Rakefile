require 'erb'
require 'rubygems'
require 'ruby-debug'

task :default => [:html, :epub, :pdf] do |t|
  t.prerequsites.each{|p|
    rake p
  }
end

task :dist do
  sh 'tar cvzfh AdminNotes.tgz AdminNotes'
  sh 'cat install AdminNotes.tgz > AdminNotes.bin; rm AdminNotes.tgz; chmod +x AdminNotes.bin'
  puts '*** AdminNotes.bin created ***'
end

targets = Rake.application.top_level_tasks

target = ''
%w[html pdf epub].each{|fmt|
  if targets.include? fmt
    target = ".#{fmt}_rst" 
  end
}

puts "target = #{target}"

task :usage do
  puts "Usage: rake html, epub or pdf"
end

contents = Dir.glob('*.erb').map{|f| f=~/(\w+)\.erb/ && $1}
puts "contents=#{contents.inspect}"

[:html, :epub, :pdf].each{|tgt|
  task tgt => contents.map{|c| "#{c}.#{tgt}_rst"} do |t|
    contents.each{|c|
      File.rename "#{c}.#{tgt}_rst", "#{c}.rst"
    }
    sh "make #{tgt}"
  end
}

directory 'images'

rule target => '.erb' do |t|
  File.open(t.name, 'w'){|f|
    erb = ERB.new(File.read(t.prerequisites.first))
    erb.result(binding).each_line{|l|
      if l =~ /http:\/\/alb\.anagix\.com:8180\/myGyazo\/data\/(.*.png)/
        image = $1
        Dir.chdir('images'){
          unless File.exist?(image)
            puts "wget #{l.chomp.strip}"
            system "wget #{l.chomp.strip}"
          end
        }
        f.puts "\n" + l.sub(/^/, '.. ')
        f.puts "\n.. image:: images/#{image}"
        f.puts '    :scale: 75%' # if target.include? 'html' 
#        f.puts '    :width: 3in' if target.include? 'pdf' 
        f.puts "    :target: #{l}"
      else
        f.puts l
      end
    }
  }
  puts "*** #{t.name} created"
end    
