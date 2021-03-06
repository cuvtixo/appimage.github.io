---
layout: app

permalink: /Eximchain_Wallet/
description: Eximchain Wallet web and electron app
license: MIT

icons:
  - Eximchain_Wallet/icons/256x258/eximchainwallet.png

screenshots:
  - Eximchain_Wallet/screenshot.png

authors:
  - name: Eximchain
    url: https://github.com/Eximchain

links:
  - type: GitHub
    url: Eximchain/EximchainWallet
  - type: Download
    url: https://github.com/Eximchain/EximchainWallet/releases

desktop:
  Desktop Entry:
    Name: Eximchain Wallet
    Comment: Eximchain Wallet web and electron app
    Exec: AppRun
    Terminal: false
    Type: Application
    Icon: eximchainwallet
    X-AppImage-Version: 0.1.2-beta
    X-AppImage-BuildId: b11d08b0-289c-11a9-038b-fbf49c545804
    Categories: Finance
  AppImageHub:
    X-AppImage-Signature: no valid OpenPGP data found. the signature could not be verified.
      Please remember that the signature file (.sig or .asc) should be the first file
      given on the command line.
    X-AppImage-Type: 2
    X-AppImage-Architecture: x86_64
    X-AppImage-Payload-License: MIT

electron:
  main: main.js
  description: Eximchain Wallet web and electron app
  repository: https://github.com/Eximchain/EximchainWallet
  engines:
    node: ">= 8.0.0"
    npm: ">= 5.0.0"
  dependencies:
    "@ledgerhq/hw-app-eth": 4.7.3
    "@ledgerhq/hw-transport-node-hid": 4.7.6
    "@ledgerhq/hw-transport-u2f": 4.12.0
    babel-polyfill: 6.26.0
    bip39: 2.5.0
    bn.js: 4.11.8
    bootstrap-sass: 3.3.7
    classnames: 2.2.5
    electron-updater: 2.21.10
    ethereum-blockies-base64: 1.0.2
    ethereumjs-abi: git://github.com/ethereumjs/ethereumjs-abi.git#09c3c48fd3bed143df7fa8f36f6f164205e23796
    ethereumjs-tx: 1.3.4
    ethereumjs-util: 5.1.5
    ethereumjs-wallet: 0.6.0
    font-awesome: 4.7.0
    hdkey: 0.8.0
    html2canvas: 1.0.0-alpha.12
    idna-uts46: 1.1.0
    jsonschema: 1.2.4
    lodash: 4.17.5
    moment: 2.22.1
    moment-timezone: 0.5.14
    mycrypto-eth-exists: 1.0.0
    mycrypto-shepherd: 1.4.0
    normalizr: 3.2.4
    qrcode: 1.2.0
    qrcode.react: 0.8.0
    query-string: 6.0.0
    rc-slider: 8.6.0
    react: 16.3.2
    react-copy-to-clipboard: 5.0.1
    react-datetime: 2.14.0
    react-dom: 16.3.2
    react-markdown: 3.3.0
    react-redux: 5.0.7
    react-router-dom: 4.2.2
    react-router-redux: 4.0.8
    react-select: 1.2.1
    react-stepper-horizontal: 1.0.9
    react-transition-group: 2.3.1
    redux: 3.7.2
    redux-logger: 3.0.6
    redux-saga: 0.16.0
    rskjs-util: 1.0.3
    scryptsy: 2.0.0
    semver: 5.5.0
    trezor.js: 6.17.5
    uuid: 3.2.1
    wallet-address-validator: 0.1.6
    whatwg-fetch: 2.0.3
    zxcvbn: 4.4.2
  resolutions:
    "*/**/@types/react": 16.3.11
  lint-staged:
    "*.{ts,tsx}":
    - prettier --write --config ./.prettierrc --config-precedence file-override
    - git add
  freezer:
  - package.json
  - common/freezer.ts
  - common/store.ts
  - common/libs/decrypt.ts
  - common/libs/signing.ts
---
