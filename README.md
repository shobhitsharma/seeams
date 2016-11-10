# Editor

A minimalistic yet comprehensive CMS Editor application for [Electron runtime](http://electron.atom.io). Tested on OSX, Windows and Linux.  

## Development

```bash
# Installation
$ npm install

# Runner
$ npm start

# Builds `dist` for shipping
$ npm run release

# Unit tests (*.spec.js)
$ npm test

# End to end tests (*.e2e.js)
$ npm run e2e

# Code coverage
$ npm run coverage
```
Application manifests separate interpolable packages due to compilation of C modules at `/package.json` and `/app/package.json`.
ES6 syntax for `src` and Vanilla/CommonJS for `app` due to native support. 

## Architecture

- `src` - ES6 scripts to be transpiled containing core functionality
- `app` - Holds static assests container and helpers

The build process compiles all stuff from the `src` folder and puts it into the `app` folder, so after the build has finished, your `app` folder contains the full, runnable application.

## Resources

- [electron-mocha](https://github.com/jprichardson/electron-mocha) test runner
- [chai](http://chaijs.com/api/assert/) assertion library
- [spectron](http://electron.atom.io/spectron/) E2E Testing
- [electron-builder](https://github.com/electron-userland/electron-builder)
- [istanbul](http://gotwarlost.github.io/istanbul/) code coverage tool
- Electron [CI Plugging](https://github.com/atom/electron/blob/master/docs/tutorial/testing-on-headless-ci.md) ([Travis CI](https://travis-ci.org/) covers testing on OSX and Linux and [App Veyor](https://www.appveyor.com) on Windows)

# License

Released under the MIT license.
