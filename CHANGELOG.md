# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [2.0.0] - 2026-02-01

### Changed
- **BREAKING**: Updated to use `@xterm/xterm` ^6.0.0 (new scoped package name)
- **BREAKING**: Dropped support for `xterm` 4.x (use v1.x for older versions)
- Updated TypeScript to ^5.7.0
- Updated imports to use `@xterm/xterm` instead of deprecated `xterm` package

### Migration Guide
To upgrade from v1.x to v2.x:

1. Update your package.json to use `@xterm/xterm` instead of `xterm`:
   ```bash
   npm uninstall xterm
   npm install @xterm/xterm@^6.0.0
   ```

2. Update your imports:
   ```js
   // Before (v1.x)
   import {Terminal} from 'xterm';

   // After (v2.x)
   import {Terminal} from '@xterm/xterm';
   ```

3. The `xterm-link-provider` API remains unchanged.

## [1.3.1] - 2021-04-12
- Previous release supporting xterm 4.x
