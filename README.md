# plymouth-stargate

Stargate SG-1 Plymouth boot splash theme.

## Design Goals

- Style: technical drawing and/or futuristic comic style.
- 7 chevrons light one after another. Last chevron is at the top.
  The order is according to [stargatewiki: dialing computer](https://en.stargatewiki.noip.me/images/1/19/Dialing_computer_%28Unending%29.jpg).

## Structure

```
stargate.plymouth          # theme descriptor
stargate.script            # animation logic
images/
  logo.png                 # Stargate SG-1 logo
  spinner-0.png .. 11.png  # 12-frame chevron spinner
  box.png, lock.png, entry.png, bullet.png  # dialog assets
```

## Colors

See `images-src/stargate.svg`:

- grey `808080ff`
- orange `ff6600ff`

## Install

```bash
sudo cp -r . /usr/share/plymouth/themes/stargate
sudo plymouth-set-default-theme -R stargate
```

See also [archwiki about plymouth](https://wiki.archlinux.org/title/Plymouth).

## Test (without reboot)

Runs the previously installed theme for 12 seconds, then quits.

```bash
su -s
plymouthd; plymouth --show-splash; sleep 12; plymouth --quit
```

## License and Attribution

Distributed under the [GNU General Public License v3.0](https://www.gnu.org/licenses/gpl-3.0.html).

The combined theme is GPL-3.0 because it incorporates GPL-3.0 assets
(see `LICENSE` for the full text).

### Image credits

- Stargate glyphs derived from Stargate-color.svg by RufusLynx, which
  in turn is derived from Stargate-color.png by Stefan-Xp,
  via Wikimedia Commons (Alphathon/'æɫfə.θɒn/).
  - [Stargate.svg](https://commons.wikimedia.org/wiki/File:Stargate.svg)
  - Original license: [CC BY-SA 3.0](http://creativecommons.org/licenses/by-sa/3.0/)
  - These assets remain under CC BY-SA 3.0 per their original terms.
- A subset of the PNGs in Aditya Shakya's
  [motion plymouth theme](https://github.com/adi1090x/plymouth-themes/tree/master/pack_3/motion).
  Re-sized and re-colored.
  - Original license: [GPL-3.0](https://www.gnu.org/licenses/gpl-3.0.html)

### Code credits

- Animation script based on `monoarch` by Marco Buzzanca,
  originally [MIT](https://opensource.org/licenses/MIT),
  re-licensed to GPL-3.0 as part of this combined work.

## References

- [plymouth-themes](https://github.com/adi1090x/plymouth-themes)
  ([previews here](https://xdaforums.com/t/bootanimations-collection.3721978/#post-74901989))
- [gnome-look original](https://www.gnome-look.org/p/1009450/)

Design:

- [SG1 wallpapers](https://wallpaperaccess.com/stargate-sg1)
  like [this](https://wallpaperaccess.com/full/5668368.jpg) but in stargate sg1 blue
  or [this](https://wallpaperaccess.com/full/5668397.jpg) for the base for technical drawing
