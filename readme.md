# Quantum Mechanical Keyboard Firmware

## Rob Erskine's fork

Hi there, I recently [wrote a blog post on getting up and running with QMK with my GMMK Pro in order to support custom RGB support for custom Layers](https://roberskine.com/blog/gmmk-pro-qmk-resolving-stm32-dfu-device-has-no-driver/).

The relevant code for my usecase can be found in `keyboards/gmmk/pro/rev1/ansi/keymaps/default`. (i tried making my own profile in viapro and rob, but ending up just overwriting the default).

You can clone this repo, but I recommend making your own fork off of the original. From there, overwrite the files in the path above with the code I have here.

Once you have that, you can then run `qmk compile -kb gmmk/pro/rev1/ansi -km default` which will use the default profile to create new firmware.

This will create a new `gmmk_pro_rev1_ansi_default.bin` firmware file in the root of the directory. You can then flash this custom firmware using QMK Toolbox.

If you need to make changes to your keymaps, you won't need to reflash. You should be able to use VIA to make changes moving forward.

If you want to change the logic of the RGB lighting, you will however need to make changes to the `keyboards/gmmk/pro/rev1/ansi/keymaps/default/keymap.c` file. 

---

[![Current Version](https://img.shields.io/github/tag/qmk/qmk_firmware.svg)](https://github.com/qmk/qmk_firmware/tags)
[![Discord](https://img.shields.io/discord/440868230475677696.svg)](https://discord.gg/Uq7gcHh)
[![Docs Status](https://img.shields.io/badge/docs-ready-orange.svg)](https://docs.qmk.fm)
[![GitHub contributors](https://img.shields.io/github/contributors/qmk/qmk_firmware.svg)](https://github.com/qmk/qmk_firmware/pulse/monthly)
[![GitHub forks](https://img.shields.io/github/forks/qmk/qmk_firmware.svg?style=social&label=Fork)](https://github.com/qmk/qmk_firmware/)

This is a keyboard firmware based on the [tmk\_keyboard firmware](https://github.com/tmk/tmk_keyboard) with some useful features for Atmel AVR and ARM controllers, and more specifically, the [OLKB product line](https://olkb.com), the [ErgoDox EZ](https://ergodox-ez.com) keyboard, and the Clueboard product line.

## Documentation

* [See the official documentation on docs.qmk.fm](https://docs.qmk.fm)

The docs are powered by [Docsify](https://docsify.js.org/) and hosted on [GitHub](/docs/). They are also viewable offline; see [Previewing the Documentation](https://docs.qmk.fm/#/contributing?id=previewing-the-documentation) for more details.

You can request changes by making a fork and opening a [pull request](https://github.com/qmk/qmk_firmware/pulls), or by clicking the "Edit this page" link at the bottom of any page.

## Supported Keyboards

* [Planck](/keyboards/planck/)
* [Preonic](/keyboards/preonic/)
* [ErgoDox EZ](/keyboards/ergodox_ez/)
* [Clueboard](/keyboards/clueboard/)
* [Cluepad](/keyboards/clueboard/17/)
* [Atreus](/keyboards/atreus/)

The project also includes community support for [lots of other keyboards](/keyboards/).

## Maintainers

QMK is developed and maintained by Jack Humbert of OLKB with contributions from the community, and of course, [Hasu](https://github.com/tmk). The OLKB product firmwares are maintained by [Jack Humbert](https://github.com/jackhumbert), the Ergodox EZ by [ZSA Technology Labs](https://github.com/zsa), the Clueboard by [Zach White](https://github.com/skullydazed), and the Atreus by [Phil Hagelberg](https://github.com/technomancy).

## Official Website

[qmk.fm](https://qmk.fm) is the official website of QMK, where you can find links to this page, the documentation, and the keyboards supported by QMK.
