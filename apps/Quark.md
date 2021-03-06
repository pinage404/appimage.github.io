---
layout: app

permalink: /Quark/
description: One software sketchbook for rapid prototyping and development of your projects.

icons:
  - Quark/icons/128x128/quark.png

screenshots:
  - Quark/screenshot.png

authors:

links:

desktop:
  Desktop Entry:
    Name: Quark
    Comment: One software sketchbook for rapid prototyping and development of your projects.
    Exec: AppRun
    Terminal: false
    Type: Application
    Icon: quark
    StartupWMClass: Quark
    X-AppImage-Version: 0.1.12
    Categories: IDE
    X-AppImage-BuildId: 1JaKKUZQkEzoXzx7g1xrB10tBOR
  AppImageHub:
    X-AppImage-Signature: no valid OpenPGP data found. the signature could not be verified.
      Please remember that the signature file (.sig or .asc) should be the first file
      given on the command line.
    X-AppImage-Type: 2
    X-AppImage-Architecture: x86_64

electron:
  homepage: https://quarkjs.io
  version: 0.1.12
  description: One software sketchbook for rapid prototyping and development of your
    projects.
  main: index.js
  bin: index.js
  dependencies:
    "@babel/core": "^7.3.4"
    "@babel/preset-react": "^7.0.0"
    "@squirtle/api": file:./../@squirtle/api
    "@vue/web-component-wrapper": "^1.2.0"
    babel-loader: "^8.0.5"
    builtin-modules: "^3.0.0"
    chart.js: "^2.7.3"
    chokidar: "^2.1.2"
    css-loader: "^2.1.0"
    electron-log: "^3.0.1"
    electron-store: "^2.0.0"
    electron-updater: "^4.0.6"
    extract-text-webpack-plugin: "^3.0.2"
    firmata: "^2.0.0"
    fs-extra: "^7.0.1"
    ionic: "^4.10.2"
    johnny-five: "^0.15.0"
    markdown-it: "^8.4.2"
    memory-fs: "^0.4.1"
    node-pty: "^0.7.8"
    node-sass: "^4.11.0"
    npm: "^6.8.0"
    p5: "^0.7.3"
    raw-loader: "^1.0.0"
    sass-loader: "^7.1.0"
    serialport: "^7.1.4"
    ts-loader: "^5.3.3"
    typescript: "^3.3.3333"
    url-loader: "^1.1.2"
    vscode-languageserver-types: "^3.14.0"
    vue: "^2.6.8"
    vue-loader: "^15.7.0"
    vue-style-loader: "^4.1.2"
    vue-template-compiler: "^2.6.8"
    webpack: "^4.29.6"
    webpack-merge: "^4.2.1"
    webpack-node-externals: "^1.7.2"
  license: ISC
  tilt:
    appId: io.quarkjs
    copyright: Copyright © 2019 Nishkal Kashyap
    productName: Quark
    artifactName: "${productName}-${os}-${arch}-${version}.${ext}"
    asar: true
    asarUnpack:
    - definitions-unpacked
    files:
    - "**/*"
    - "!**/node_modules/*/{test,__tests__,tests,powered-test,example,examples}"
    - "!**/node_modules/.bin"
    - "!**/*.{iml,o,hprof,orig,pyc,pyo,rbc,swp,csproj,sln,xproj}"
    - "!.editorconfig"
    - "!**/._*"
    - "!**/{.DS_Store,.git,.hg,.svn,CVS,RCS,SCCS,.gitignore,.gitattributes}"
    - "!**/{__pycache__,thumbs.db,.flowconfig,.idea,.vs,.nyc_output}"
    - "!**/{appveyor.yml,.travis.yml,circle.yml}"
    - "!**/{npm-debug.log,yarn.lock,.yarn-integrity,.yarn-metadata.json}"
    - "!dist"
    - "!build"
    - "!.vscode"
    - "!definitions"
    directories:
      output: build
      buildResources: buildResources
    win:
      target: nsis
    nsis:
      oneClick: false
      perMachine: true
      allowToChangeInstallationDirectory: true
      license: LICENSE
      runAfterFinish: true
      createDesktopShortcut: true
      createStartMenuShortcut: true
    linux:
      target: AppImage
    appImage:
      systemIntegration: ask
      license: LICENSE
    mac:
      target: default
      category: public.app-category.utilities
    extraResources:
    - from: definitions
      to: definitions
---
