WindowsでRubyの開発環境構築の流れ
==================================

Install ruby
-------------------

RubyをWindowsに追加するため、 rubyinstaller_ を利用します。
Ruby+Devkit 2.4.4-1 (x64)  をDownloadして、Install します。

Install する際に、InternetからPackagesをDownloadします。
なので、Proxy環境の下に設定する場合、Proxy設定が必要です。
Windowsの場合以下のように、環境変数に追加すれば良いです。

.. code-block:: sh

    　http_proxy　http://user:pasword@proxy.server.address:port
      https_proxy http://user:pasword@proxy.server.address:port
      ftp_proxy http://user:pasword@proxy.server.address:port

Install vscode
------------------

Micorsoft の　Visual Studio Code　をInstallします。
Install後、Rubyの以下のPackageを追加します。

.. code-block:: sh

    $ gem install ruby-debug-ide debase ← VSCodeのRubyエクステンションに必要
    $ gem install reek rubocop fasterer debride ruby-lint ← Lintに必要。全て必要かどうかはわからない。
    $ gem install rcodetools ← AutoCompleteに必要
    $ gem install fastri ← rcodetoolsインストール時に追加インストールを推奨され

Visual studio code の設定は以下の行を追加

.. code-block:: sh

    # settings.json
    "ruby.lint": {
    "reek": true,
    "rubocop": true,
    "ruby": false, //Runs ruby -wc
    "fasterer": true,
    "debride": true,
    "ruby-lint": true
  }

ruby codeをJupyterで動かす
-----------------------------

See jupyter_ruby_ for more detail.

.. _jupyter_ruby: https://github.com/SciRuby/iruby

.. _rubyinstaller: https://rubyinstaller.org/

.. _mysys2: http://www.msys2.org/
