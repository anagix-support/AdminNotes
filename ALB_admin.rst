=================
よくある管理ワーク
=================
サインアップ
------------
Loginの前に Sign upしてください。Sign upボタンはページの右上にあります。

デフォルトでは、メールによる認証はしておりませんので、Sign up
すればすぐにLogin できます。


.. http://alb.anagix.com:8180/myGyazo/data/0a7d3b967397843f015133eda1bc5fcf.png

.. image:: images/0a7d3b967397843f015133eda1bc5fcf.png
    :scale: 75%
    :target: http://alb.anagix.com:8180/myGyazo/data/0a7d3b967397843f015133eda1bc5fcf.png

Sign up後、システムの不具合により一見Loginしているように見えますが、
実際は Loginしていないのであらためてログインしてください。

一般ユーザから管理者になる
-----------------------
管理者にならないと、ALTAのライセンス登録やプロジェクトのアクセス権の設定などができません。

一般ユーザを管理者に変えるには、管理者としてログインし、そのユーザにAdministratorを設定します。

以下の手順は、ALBパーソナル版の場合の例です。

（１）まず、admin@anagix.com (パスワードは anagixalb　でログインしてください）。

.. http://alb.anagix.com:8180/myGyazo/data/fc40955bb33747ac403c99905f6e62df.png

.. image:: images/fc40955bb33747ac403c99905f6e62df.png
    :scale: 75%
    :target: http://alb.anagix.com:8180/myGyazo/data/fc40955bb33747ac403c99905f6e62df.png

（２）次に、Projectタブに移動してください。


.. http://alb.anagix.com:8180/myGyazo/data/717c47e0cae0b9ce81357b8b3cab17bd.png

.. image:: images/717c47e0cae0b9ce81357b8b3cab17bd.png
    :scale: 75%
    :target: http://alb.anagix.com:8180/myGyazo/data/717c47e0cae0b9ce81357b8b3cab17bd.png

（３）表の中から、対象のUser（この場合 Seijiro Moriyama）を選択します。


.. http://alb.anagix.com:8180/myGyazo/data/064e2b0ebabfe3e8174f0e3981b33e38.png

.. image:: images/064e2b0ebabfe3e8174f0e3981b33e38.png
    :scale: 75%
    :target: http://alb.anagix.com:8180/myGyazo/data/064e2b0ebabfe3e8174f0e3981b33e38.png

（４）右上の Edit Userをクリックします。


.. http://alb.anagix.com:8180/myGyazo/data/beb050c0adb84649186ae54162bd43b2.png

.. image:: images/beb050c0adb84649186ae54162bd43b2.png
    :scale: 75%
    :target: http://alb.anagix.com:8180/myGyazo/data/beb050c0adb84649186ae54162bd43b2.png

Administratorにチェックを入れます。Saveすると有効になります。

プロジェクトを見えるようにする
--------------------------

HOMEタブ画面で、プロジェクトを選択しようとしても表示されないのは、ログインしたユーザがその
プロジェクトへのアクセスを許可されていないからです。

ユーザは、アクセスを許可されたプロジェクトしか見たり編集したりすることができません。

アクセスの許可は、管理者が行います。まず、管理者としてログインし、Projectタブに
移動します。


.. http://alb.anagix.com:8180/myGyazo/data/568ddfe9ed252c7bd4ca6634af8cc02e.png

.. image:: images/568ddfe9ed252c7bd4ca6634af8cc02e.png
    :scale: 75%
    :target: http://alb.anagix.com:8180/myGyazo/data/568ddfe9ed252c7bd4ca6634af8cc02e.png

（１）プロジェクトからアサインする方法
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

対象のプロジェクトをクリックしてプロジェクトのページに入り、Add new user or groupをクリック


.. http://alb.anagix.com:8180/myGyazo/data/1c8199fcd64f1ac546aae7244ea17d79.png

.. image:: images/1c8199fcd64f1ac546aae7244ea17d79.png
    :scale: 75%
    :target: http://alb.anagix.com:8180/myGyazo/data/1c8199fcd64f1ac546aae7244ea17d79.png

対象のユーザを選択して Create Project Assignmentを実行。


.. http://alb.anagix.com:8180/myGyazo/data/d725fb0b098758f29368ff8381d19d6b.png

.. image:: images/d725fb0b098758f29368ff8381d19d6b.png
    :scale: 75%
    :target: http://alb.anagix.com:8180/myGyazo/data/d725fb0b098758f29368ff8381d19d6b.png

（２）ユーザとプロジェクトを指定してアサインする方法
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Projectタブのページで、New Project Assignmentを選択する。


.. http://alb.anagix.com:8180/myGyazo/data/079c6817b575052cb94f962204c85694.png

.. image:: images/079c6817b575052cb94f962204c85694.png
    :scale: 75%
    :target: http://alb.anagix.com:8180/myGyazo/data/079c6817b575052cb94f962204c85694.png

UserとProjectを選択し、Create Project Assignment。


.. http://alb.anagix.com:8180/myGyazo/data/11aab4b8ae3426931501fdf54df6a1bd.png

.. image:: images/11aab4b8ae3426931501fdf54df6a1bd.png
    :scale: 75%
    :target: http://alb.anagix.com:8180/myGyazo/data/11aab4b8ae3426931501fdf54df6a1bd.png

Edit Allowedにチェックを入れると、編集を許可することができます。

ALTAのライセンス登録
----------------------------

ALTAを使用するマシーンのMACアドレスをALBサーバに設定していただく必要があります。

Wikipediaによると：
”Media Access Control address）は、ネットワーク上で、各ノードを識別するために設定されているLANカードなどのネットワーク機器のハードウェアに（原則として）一意に割り当てられる物理アドレスである。”

登録前に、ALTAからALBサーバに接続すると、以下のようなエラー表示画面がでます。


.. http://alb.anagix.com:8180/myGyazo/data/3df72367930f4f0e78217c67e865b2ae.png

.. image:: images/3df72367930f4f0e78217c67e865b2ae.png
    :scale: 75%
    :target: http://alb.anagix.com:8180/myGyazo/data/3df72367930f4f0e78217c67e865b2ae.png

管理者としてALBにログインし、以下の操作を行ってください。

*Step1:* ALBサーバのグループ作成の機能を利用して、まずAdminタブからGroupを新規に作成します
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^


.. http://alb.anagix.com:8180/myGyazo/data/1dfa59620bf61cd902fab303a3a690ab.png

.. image:: images/1dfa59620bf61cd902fab303a3a690ab.png
    :scale: 75%
    :target: http://alb.anagix.com:8180/myGyazo/data/1dfa59620bf61cd902fab303a3a690ab.png

注意：Group（名前はALBサーバのMACアドレス）がすでに作成されている場合は、そのグループを Editしてください。

New Groupをクリックすると以下のようなグループ作成画面がでます。


.. http://alb.anagix.com:8180/myGyazo/data/5efe4c43a6b509f13486beeca8b60ba4.png

.. image:: images/5efe4c43a6b509f13486beeca8b60ba4.png
    :scale: 75%
    :target: http://alb.anagix.com:8180/myGyazo/data/5efe4c43a6b509f13486beeca8b60ba4.png

*Step2:* Groupの名前を、ALBサーバのMACアドレスにする
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

グループ名としてALBサーバのMACアドレスから英数字以外の文字（：や ー）を消去した12桁の文字列を入力して
ください。

MACアドレスは、以下の方法で調べることができます。ALBサーバにログインし、ifconfigコマンドを実行すると
表示されるHWaddrがMACアドレスです。


.. http://alb.anagix.com:8180/myGyazo/data/bdd7c663ba8ba7081e9d260754230147.png

.. image:: images/bdd7c663ba8ba7081e9d260754230147.png
    :scale: 75%
    :target: http://alb.anagix.com:8180/myGyazo/data/bdd7c663ba8ba7081e9d260754230147.png

ifconfig: command not foundとなる場合は、/sbin/ifconfig と入力してください。

*Step3:* Description欄にALTAを使用するマシーンのMACアドレスを1台づつ記述する
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

ALTA側のマシーンのMACアドレスは、一番最初のエラー表示画面に出力されています。Windowsの
場合、コマンドプロンプトで、ipconfig コマンドを使って調べることができます。


.. http://alb.anagix.com:8180/myGyazo/data/32017404086e955ac0adcd15cef44c67.png

.. image:: images/32017404086e955ac0adcd15cef44c67.png
    :scale: 75%
    :target: http://alb.anagix.com:8180/myGyazo/data/32017404086e955ac0adcd15cef44c67.png

”イーサネットアダプタローカルエリア接続”の”物理アドレス"がMACアドレスです。

LTspice用のシンボルを作る
-----------------------

プロジェクトを開きます。この例は、ALTA sampleです。


.. http://alb.anagix.com:8180/myGyazo/data/ec34bd5cdcb2c7937aca0d6467b8b031.png

.. image:: images/ec34bd5cdcb2c7937aca0d6467b8b031.png
    :scale: 75%
    :target: http://alb.anagix.com:8180/myGyazo/data/ec34bd5cdcb2c7937aca0d6467b8b031.png

回路図シンボルの入ったライブラリ（この例では、analogLib）を選択します。


.. http://alb.anagix.com:8180/myGyazo/data/70efd57d9b8ed3577ff723b6b530ed2b.png

.. image:: images/70efd57d9b8ed3577ff723b6b530ed2b.png
    :scale: 75%
    :target: http://alb.anagix.com:8180/myGyazo/data/70efd57d9b8ed3577ff723b6b530ed2b.png

(ALTA Import | Download | ADE)の表示から、Downloadを選びます。

シンボルを固めたファイルがダウンロードされます。この場合、analogLib.zipができます。


.. http://alb.anagix.com:8180/myGyazo/data/f2c437b523137b6437eb4a06f985c798.png

.. image:: images/f2c437b523137b6437eb4a06f985c798.png
    :scale: 75%
    :target: http://alb.anagix.com:8180/myGyazo/data/f2c437b523137b6437eb4a06f985c798.png

ダウンロードされたzipファイルをLTspiceがインストールされた場所、例えば c:\Program Files\LTC\LTspiceIV\lib\sym
の下に展開してください。

以下のようにLTspiceで、Componentを選択するフォームで、[analogLib]の表示がでていれば
成功です。analogLibのシンボルを使った回路図作成ができるようになります。


.. http://alb.anagix.com:8180/myGyazo/data/904a857a0f65c80c44eb78248de415fd.png

.. image:: images/904a857a0f65c80c44eb78248de415fd.png
    :scale: 75%
    :target: http://alb.anagix.com:8180/myGyazo/data/904a857a0f65c80c44eb78248de415fd.png

以上
