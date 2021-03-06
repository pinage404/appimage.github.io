---
layout: app

permalink: /CodePilot.ai/
description: Quickly find code you can reuse or learn from

icons:
  - CodePilot.ai/icons/256x256/codepilot-ai.png

screenshots:
  - CodePilot.ai/screenshot.png

authors:

links:

desktop:
  Desktop Entry:
    Name: CodePilot.ai
    Comment: Quickly find code you can reuse or learn from
    Exec: AppRun
    Terminal: false
    Type: Application
    Icon: codepilot-ai
    X-AppImage-Version: 4.4.2
    X-AppImage-BuildId: 023a31b0-99c7-11a8-0f94-7fc66971dccb
    MimeType: x-scheme-handler/codepilot
    Categories: Development
  AppImageHub:
    X-AppImage-Signature: no valid OpenPGP data found. the signature could not be verified.
      Please remember that the signature file (.sig or .asc) should be the first file
      given on the command line.
    X-AppImage-Type: 2
    X-AppImage-Architecture: x86_64

electron:
  description: Quickly find code you can reuse or learn from
  license: SEE LICENSE IN license.txt
  main: "./dist/electron/main.js"
  lint-staged:
    src/renderer/**/*.{vue,scss}:
    - cross-env NODE_ENV=production stylelint --fix
    - git add
    src/**/*.{js,vue}:
    - cross-env NODE_ENV=production eslint --fix
    - cross-env NODE_ENV=production prettier --write
    - git add
    test/**/*.js:
    - cross-env NODE_ENV=production eslint --fix
    - cross-env NODE_ENV=production prettier --write
    - git add
    ".electron-vue/**/*.js":
    - cross-env NODE_ENV=production eslint --fix
    - cross-env NODE_ENV=production prettier --write
    - git add
  dependencies:
    analytics-node: "^3.2.x"
    apollo-cache-inmemory: "^1.2.5"
    apollo-client: "^2.3.5"
    apollo-link-context: "^1.0.8"
    apollo-link-http: "^1.5.4"
    auto-launch: "^5.0.x"
    autosize: "^4.0.x"
    axios: "^0.18.0"
    babel-cli: "^6.26.0"
    backtrace-js: "^0.0.11"
    base-64: "^0.1.x"
    cuid: "^2.1.x"
    date-fns: "^1.29.x"
    electron-settings: "^3.2.0"
    electron-updater: "^2.23.3"
    escape-html: "^1.0.x"
    file-icons-js: "^1.0.x"
    findandreplacedomtext: "^0.4.6"
    firebase: 4.8.0
    font-awesome: "^4.7.x"
    graceful-fs: "^4.1.11"
    graphql: "^0.13.x"
    graphql-tag: "^2.9.x"
    html-entities: "^1.2.x"
    html-to-markdown: "^1.0.x"
    lodash: "^4.17.x"
    lucene-query-parser: "^1.2.0"
    markdown-it: "^8.4.1"
    minimist: "^1.2.x"
    mkdirp: "^0.5.x"
    monaco-editor: "^0.10.1"
    node-fetch: "^2.1.2"
    node-machine-id: "^1.1.x"
    normalize.css: "^8.0.x"
    p-queue: "^2.4.1"
    parse-full-name: "^1.2.x"
    rxjs: "^5.5.11"
    superagent: "^3.6.x"
    systeminformation: "^3.42.4"
    tailwindcss: "^0.5.3"
    temp: "^0.8.x"
    url: "^0.11.0"
    v-tooltip: "^2.0.0-rc.33"
    vscode-ripgrep: "^1.0.1"
    vue: "^2.5.x"
    vue-electron: "^1.0.x"
    vue-global-events: "^1.0.x"
    vue-monaco: "^0.1.x"
    vue-multiselect: "^2.1.0"
    vue-octicon: "^2.1.x"
    vue-slicksort: "^0.1.8"
    vue-tour: "^1.0.1"
    vuelidate: "^0.6.x"
    vuex: "^3.0.x"
    youtube-search-promise: "^1.0.3"
---
