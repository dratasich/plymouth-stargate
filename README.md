# plymouth-stargate-sg1

Stargate SG-1 Plymouth boot splash theme.

## Design Goals

- Style: technical drawing and/or futuristic comic style.
- 7 chevrons light one after another. Last chevron is at the top.
  The order is according to [stargatewiki: dialing computer](https://en.stargatewiki.noip.me/images/1/19/Dialing_computer_%28Unending%29.jpg)

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

- See `images-src/stargate.svg`
- box 1px `808080ff`

## Install

```bash
sudo cp -r . /usr/share/plymouth/themes/stargate
sudo plymouth-set-default-theme stargate
```

## Test (without reboot)

```bash
sudo plymouthd
sudo plymouth --show-splash
sleep 5
sudo plymouth --quit
```

## Licence and Attribution

Images are derived from

- Alphathon /'æɫfə.θɒn/ (talk)Glyphs derived from Stargate-color.svg by RufusLynx, which in turn is derived from Stargate-color.png by Stefan-Xp, CC BY-SA 3.0 <http://creativecommons.org/licenses/by-sa/3.0/>, via Wikimedia Commons.
  - [Stargate.svg](https://commons.wikimedia.org/wiki/File:Stargate.svg)

and shared under the same license [CC BY-SA 3.0](http://creativecommons.org/licenses/by-sa/3.0/).

The plymouth theme is based on [monoarch]()
by Marco Buzzanca distributed under [MIT License](https://opensource.org/licenses/MIT).

## References

- [plymouth-themes](https://github.com/adi1090x/plymouth-themes)
- [gnome-look original](https://www.gnome-look.org/p/1009450/)

Design:

- [SG1 wallpapers](https://wallpaperaccess.com/stargate-sg1)
  like [this](https://wallpaperaccess.com/full/5668368.jpg) but in stargate sg1 blue
  or [this](https://wallpaperaccess.com/full/5668397.jpg) for the base for technical drawing
