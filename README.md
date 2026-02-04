# xterm-link-provider

Create a [Link Provider](https://github.com/xtermjs/xterm.js/blob/a73fe62b7aedcd331e01130b92d7e753bb5be55b/typings/xterm.d.ts#L1125) for [xterm.js](https://github.com/xtermjs/xterm.js/) using regex (based on xterm-addon-web-links' WebLinkProvider [class](https://github.com/xtermjs/xterm.js/blob/bd6676d3b6d5404e9cf46c3882f543de2fae963f/addons/xterm-addon-web-links/src/WebLinkProvider.ts))

[![npm](https://img.shields.io/npm/v/xterm-link-provider?style=for-the-badge)](https://www.npmjs.com/package/xterm-link-provider)
[![unpkg](https://img.shields.io/badge/dynamic/json?label=unpkg&query=$.version&url=https%3A%2F%2Funpkg.com%2Fxterm-link-provider%40latest%2Fpackage.json&style=for-the-badge&color=orange)](https://unpkg.com/xterm-link-provider@latest/)

## Install

```
$ npm install --save xterm-link-provider @xterm/xterm
```

**Note:** Version 2.0.0+ requires `@xterm/xterm` ^6.0.0. For older versions of xterm.js (4.x), use xterm-link-provider 1.x.

## Usage

```js
import {LinkProvider} from 'xterm-link-provider';
import {Terminal} from '@xterm/xterm';

// print clicked emojis to console

const emojiRegex = /(\p{Emoji_Presentation}+)/gu

terminal.registerLinkProvider(
  new LinkProvider(
    terminal,
    emojiRegex,
    (e, text) => {
      console.log(text)
    }
  )
)
```

## Version Compatibility

- **v2.x**: Compatible with `@xterm/xterm` ^6.0.0
- **v1.x**: Compatible with `xterm` ^4.11.0
