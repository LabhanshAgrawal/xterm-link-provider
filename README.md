# xterm-link-provider

Create a [Link Provider](https://github.com/xtermjs/xterm.js/blob/a73fe62b7aedcd331e01130b92d7e753bb5be55b/typings/xterm.d.ts#L1125) for [xterm.js](https://github.com/xtermjs/xterm.js/) using regex (based on xterm-addon-web-links' WebLinkProvider [class](https://github.com/xtermjs/xterm.js/blob/bd6676d3b6d5404e9cf46c3882f543de2fae963f/addons/xterm-addon-web-links/src/WebLinkProvider.ts))

[![npm](https://img.shields.io/npm/v/xterm-link-provider?style=for-the-badge)](https://www.npmjs.com/package/xterm-link-provider)

## Install

```
$ npm install --save xterm-link-provider
```

## Usage

```js
import {LinkProvider} from 'xterm-link-provider';

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
