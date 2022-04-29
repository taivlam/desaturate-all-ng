Prerequisites
=============

Make sure GNOME Extensions and GNOME Tweaks are installed.

On Debian-/Ubuntu-based distros, install the required packages in a terminal
emulator:
```
$ sudo apt-get install gnome-tweaks gnome-shell-extensions
```

Installation (Local)
====================

Using a terminal, execute the following commands:

```
$ git clone https://github.com/OmegaMartFan/desaturate_all.git
$ mv desaturate_all "~/.local/share/gnome-shell/extensions/desaturate_all@OmegaMartFan-on-GitHub"
```

Then press `Alt`+`F2`, type `r` in the dialog window, then press `Enter`.

(No idea what the above line actually does in GNOME - will test later.)

To Do
=====

* Get rid of keyboard shortcut
    * Remaining info has been moved here:

~~The default keyboard shortcut to toggle desaturation is `<Super>`+`e`. You can
change this shortcut key using `gsettings`. For example, to change the keyboard
shortcut to `<Ctrl>`+`e`, run the following command:~~

```
$ gsettings --schemadir \
  ~/.local/share/gnome-shell/extensions/desaturate_all@OmegaMartFan-on-GitHub/schemas \
  set org.gnome.shell.extensions.desaturate-all.keybindings toggle "['<Ctrl>E']"
```

You can now enable the extension by running `gnome-shell-extension-prefs`~~, or by
browsing to https://extensions.gnome.org/local.~~

License
=======

The code is licensed under the GPLv3 License, which can be found [here](LICENSE).
