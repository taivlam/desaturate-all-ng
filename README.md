## Prerequisites

Make sure GNOME Extensions and GNOME Tweaks are installed.

On Debian-/Ubuntu-based distros, install the required packages in a terminal
emulator:
```
$ sudo apt-get install gnome-tweaks gnome-shell-extensions
```

## Installation (Local)

Using a terminal, execute the following commands:

```
$ git clone https://github.com/OmegaMartFan/desaturate_all.git
$ mv desaturate_all "~/.local/share/gnome-shell/extensions/desaturate_all@OmegaMartFan-on-GitHub"
```

Then press `Alt`+`F2`, type `r` in the dialog window, then press `Enter`.

(No idea what the above line actually does in GNOME - will test later.)

You can now enable the extension by running `gnome-shell-extension-prefs`~~, or by
browsing to https://extensions.gnome.org/local.~~

## Goals and Maintenance Capacity

Some goals:

* Uphold the [KISS principle](https://en.wikipedia.org/wiki/KISS_principle)
    * I know, it's GNOME
    * But since GNOME's a mouse & keyboard GUI, this also stays that way
    * Turn on/off the extension manually by clicking on the painter's palette
    * So, no nonsense with "turn on automatically at night"
    * If you really want this, then ask upstream GNOME to implement this in
  its built-in Accessibility options
    * I wouldn't want this coupled with Night Light
        * just like how [Redshift](https://en.wikipedia.org/wiki/Redshift_(software))
          isn't necessary in GNOME due to [Night Light](https://help.gnome.org/users/gnome-help/stable/display-night-light.html.en)
* Keep the extension working for current releases on Debian Unstable/non-LTS
  Ubuntu
    * Though I can also explicitly indicate GNOME versions on Debian Stable,
      whenever issues arise
    * However, I will likely stop working on this when I retire my Debian
      Unstable or when System76 moves Pop!\_OS from GNOME-based COSMIC to its
      in-house Rust-based DE - whichever comes first

## To Do

* Possibly rewrite the entire extension (though no promises)
  * At least this would justify renaming this extension
* Ensure compliance with GNOME 40, 42 standards
    * Since this is rather simple, this could be easier than expected - but it
    doesn't hurt to double check
* Submit to GNOME Extensions
    * Rename extension
* Get rid of keyboard shortcut (what the heck is that compiled schema file?)
* True endgame is getting this implemented in GNOME's built-in
  Accessibility settings so this extension can be permanently retired
    * Don't misconstrue this desire for laziness
    * I don't want to be developing this (potentially) forever
* Remaining info has been moved here:

~~The default keyboard shortcut to toggle desaturation is `<Super>`+`e`. You can
change this shortcut key using `gsettings`. For example, to change the keyboard
shortcut to `<Ctrl>`+`e`, run the following command:~~

```
$ gsettings --schemadir \
  ~/.local/share/gnome-shell/extensions/desaturate_all@OmegaMartFan-on-GitHub/schemas \
  set org.gnome.shell.extensions.desaturate-all.keybindings toggle "['<Ctrl>E']"
```

## License

The code is licensed under the GPLv3 License, which can be found [here](LICENSE).
