Azureを用いて、開発するメモ
=============================

1. Azureで開発Machineを立ち上がる
-----------------------------------

Create Ubuntu machine, then setup network rules, etc (VNCはポート5901を利用するので、必ずすのポート開く)

Add data disk : https://docs.microsoft.com/en-us/azure/virtual-machines/linux/add-disk

Add vncserver : https://www.digitalocean.com/community/tutorials/how-to-install-and-configure-vnc-on-ubuntu-16-04

xfce often fail, so use the lxde desktop is better choice

.. code-block:: sh

    #!/bin/sh

    # Uncomment the following two lines for normal desktop:
    # unset SESSION_MANAGER
    # exec /etc/X11/xinit/xinitrc

    [ -x /etc/vnc/xstartup ] && exec /etc/vnc/xstartup
    [ -r $HOME/.Xresources ] && xrdb $HOME/.Xresources
    xsetroot -solid grey
    vncconfig -iconic &
    x-terminal-emulator -geometry 80x24+10+10 -ls -title "$VNCDESKTOP Desktop" &
    x-window-manager &

    lxterminal &
    /usr/bin/lxsession -s LXDE &

Install development tool : https://gist.github.com/rajmani1995/cae8a16056e44bd901a6d17d8f1a7fbf

Install anaconda and other
