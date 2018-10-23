# Polybar Break Timer

Take a break

- Mouse scroll = Set Time
- Click Left = Enable
- Click Right = Disable

Inspired in [gnome-break-timer](https://github.com/GNOME/gnome-break-timer).

## Installation

This is a [Node.js](https://nodejs.org/) module available through the
[npm registry](https://www.npmjs.com/). It can be installed using the
[`npm`](https://docs.npmjs.com/getting-started/installing-npm-packages-locally)
or
[`yarn`](https://yarnpkg.com/en/)
command line tools.

```sh
npm install polybar-break-timer -g
```

## Usage

Polybar Config:
```
; Polybar Break Timer
[module/breaktimer]
type = custom/script
format-prefix = "Break Timer "
format-foreground = ${colors.verdeclaro}
exec = polybar-break-timer $HOME/.config/polybar/.env/break-timer 20
click-left = echo left >> $HOME/.config/polybar/.env/break-timer
click-middle = echo middle >> $HOME/.config/polybar/.env/break-timer
click-right = echo right >> $HOME/.config/polybar/.env/break-timer
scroll-up = echo scrollUp >> $HOME/.config/polybar/.env/break-timer
scroll-down = echo scrollDown >> $HOME/.config/polybar/.env/break-timer
tail = true
```

And create a file in $HOME/.config/polybar/.env/break-timer.

## Dependencies

- [node-notifier](https://ghub.io/node-notifier): A Node.js module for sending notifications on native Mac, Windows (post and pre 8) and Linux (or Growl as fallback)
- [polybar-helpers](https://ghub.io/polybar-helpers): [WIP] Polybar - Helpers to create plugin/module using NodeJS
- [tail](https://ghub.io/tail): tail a file in node

## License

MIT
