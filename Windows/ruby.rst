WindowsでRubyの開発環境構築の流れ
==================================

RubyをWindowsに追加するため、 rubyinstaller_ を利用します。
Versioん 2.4　から mysys2_ が必要になります。

最初に mysys2_ をInstallします。
Install終了後に、 .bashrcに会社のProxy情報を追加します。

.. code-block:: sh

    export http_proxy="http://proxy.server.address:port"
    export https_proxy="http://proxy.server.address:port"
    export ftp_proxy="http://proxy.server.address:port"
    export rsync_proxy="http://proxy.server.address:port"

Proxy情報を追加後に、rubyinstallerを実効します。
最後にある　"ridk install"が失敗するので、一回Installerを終了して、
mysys2のConsoleで以下のコマンドを実効します。
また、rubyinstaller終了後に、環境のPathにrubyやgemの実効 command
を追加されなければ、手で追加することが必要です。

.. code-block:: sh

    ridk install

設定はここで終了



.. _rubyinstaller: https://rubyinstaller.org/

.. _mysys2: http://www.msys2.org/
