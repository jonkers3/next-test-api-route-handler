# Changelog

All notable changes to this project will be documented in this auto-generated
file. The format is based on [Conventional Commits][198]; this project adheres
to [Semantic Versioning][199].

## [4.0.0-canary.1][200] (2022-02-18)

### 💥 BREAKING CHANGES 💥

- **_package_:** **`main`, `types`, `module` keys removed from package.json.**
  `typesVersions` will be removed in the next major release.
- **_package_:** **Node12 is officially end-of-life and hence no longer
  supported by NTARH**

#### ⚙️ Build system

- Simplify package distributables using commonjs-static (webpack) and
  esm-shakable (babel) ([bd552b8][201])

#### 🧙🏿 Refactored

- **package:** update minimum node engine to 14.19.0 ([a1b4c93][202])
- **package:** use "exports" key exclusively ([e999cad][203])

### [3.1.1][1] (2022-02-18)

#### 🪄 Fixes

- Ensure compat with next\@12.1.0 ([484d702][2]) <sup>closes [#487][3]</sup>

#### 🔥 Reverted

- _"refactor: update npm scripts, linting"_ ([77ad96d][4])

## [3.1.0][5] (2022-02-11)

#### ✨ Features

- Automatically add the x-msw-bypass ([21b4b92][6])

#### ⚙️ Build system

- **deps:** bump next from 12.0.8 to 12.0.10 ([2a2f0b2][7])
- **readme:** explain MSW compat default behavior ([0ee4ce5][8])

### [3.0.3][9] (2022-02-05)

#### ⚙️ Build system

- **package:** bump node-fetch to 2.6.7 ([1e8cd85][10])

### [3.0.2][11] (2022-01-03)

#### ⚙️ Build system

- **readme:** update shields.io maintenance badge to 2022 ([84f74f5][12])

### [3.0.1][13] (2021-12-27)

#### ⚙️ Build system

- **package:** retire use of sort-package-json fork ([a925da2][14])

## [3.0.0][15] (2021-12-17)

### 💥 BREAKING CHANGES 💥

- **_src_:** **`fetch` now comes from node-fetch directly instead of
  isomorphic-unfetch**
- **_src_:** **exported `TestParameters` type has been renamed to
  `NtarhParameters`**

#### ✨ Features

- **package:** remove debug dependency (moved into dev-deps) ([d3c60cb][16])
- **src:** improved error handling; add support for new `rejectOnHandlerError`
  option ([68d30da][17])
- **src:** move test-listen functionality into NTARH; remove dependency
  ([15c899a][18])
- **src:** replace isomorphic-unfetch with node-fetch ([5a1a2ee][19])

#### 🧙🏿 Refactored

- **src:** update types ([73f44b7][20])

### [2.3.4][21] (2021-11-16)

#### 🪄 Fixes

- **src:** lazy-load contents of the "cookies" field ([854704b][22])

#### ⚙️ Build system

- Re-enable treeshaking in webpack ([9302bcc][23])

### [2.3.3][24] (2021-11-10)

#### ⚙️ Build system

- Differentiate between esm and bundler distributables ([597c249][25])

### [2.3.2][26] (2021-11-07)

#### 🪄 Fixes

- **src:** es module compatibility; no longer attempts to require() in mjs files
  ([32eafab][27])
- **src:** report parsed es module import failures properly ([cd98aab][28])

### [2.3.1][29] (2021-11-06)

#### ⚙️ Build system

- Re-enable ESM (for bundlers) integration tests ([91f08d4][30])

## [2.3.0][31] (2021-11-05)

#### ✨ Features

- Automatically parse "set-cookie" headers; available in response.cookies
  ([cd3cd95][32]) <sup>closes [#373][33]</sup>

#### 🪄 Fixes

- **src:** ensure exceptions do not prevent Jest from exiting ([8746e5f][34])
- **src:** ensure webpack does not break dynamic require on compile
  ([ae778d1][35]) <sup>closes [#378][36]</sup>
- Vastly improved error handling for those using node@<15 and/or npm@<7
  ([c216caa][37])

#### ⚙️ Build system

- Add back nullish coalescing operator babel transform for older node versions
  ([5fbb6d2][38])
- **package:** backport npm script fixes ([346e8de][39])
- **src:** fix TS bundle errors on node\@12 and node\@14 ([812e6f2][40])

#### 🔥 Reverted

- _"chore(github): enable debug mode"_ ([5034aba][41])

### [2.2.1][42] (2021-08-29)

#### ⚙️ Build system

- **license:** switch to MIT license ([de9ee17][43])

## [2.2.0][44] (2021-08-22)

#### ✨ Features

- **types:** expanded typescript support; `testApiHandler` weakly typed by
  default ([419d5fe][45])

### [2.1.3][46] (2021-08-22)

#### 🪄 Fixes

- **src:** ensure dependency resolution failure does not cause test runner to
  hang ([7916f00][47])

### [2.1.2][48] (2021-08-14)

#### 🪄 Fixes

- **src:** memoize resolver import ([74241ee][49])

#### ⚙️ Build system

- **package:** improve build-docs npm script ([33b6a34][50])
- **src:** add descriptions to TypeScript types ([1c3425c][51])

### [2.1.1][52] (2021-08-13)

#### 🪄 Fixes

- **readme:** update install instructions; fix apollo example ([fd787ca][53])

#### ⚙️ Build system

- **webpack.config:** second fix for faulty env management ([87ed12b][54])

## [2.1.0][55] (2021-08-13)

#### ✨ Features

- **src:** enable backwards compatibility all the way back to next\@9
  ([c51cf02][56]) <sup>closes [#295][57]</sup>

#### ⚙️ Build system

- **webpack.config:** do not ignore warnings ([2b14d84][58])
- **webpack.config:** fix faulty env management ([f477260][59])

#### 🔥 Reverted

- _"chore: update dependencies"_ ([f61fd8c][60]) <sup>closes [#296][61]</sup>

### [2.0.2][62] (2021-07-29)

#### ⚙️ Build system

- **external-scripts:** use latest mongodb native driver ([fd53fef][63])
- **webpack.config.js:** more robust build process ([e5c6a99][64])

### [2.0.1][65] (2021-06-27)

#### ⚙️ Build system

- Update dependencies and publish fixed apollo example ([ef32668][66])

## [2.0.0][67] (2021-06-27)

### 💥 BREAKING CHANGES 💥

- **_package.json_:** **this version (and the version before this version) no
  longer works with next@<10**

#### ✨ Features

- Add `url` and `paramsPatcher` ([ee31fa8][68])

#### ⚙️ Build system

- **package.json:** update dependencies ([2f1125c][69])
- **package.json:** update dependencies ([7583209][70])
- **package.json:** update next peer dependency to >=10.0.x ([bc5e72d][71])
- Switch to @xunnamius/conventional-changelog-projector shared config
  ([bc7eb3d][72])
- Update dependencies ([20ca255][73])

### [1.2.24][74] (2021-05-08)

#### 🪄 Fixes

- **index.ts:** next 10.2.0 compat ([af177c5][75])

#### ⚙️ Build system

- **.github/workflows:** disable old pipeline; begin transition to new pipeline
  ([364549e][76])
- **.github/workflows:** overhaul pipeline workflows ([4db5d04][77])
- **.github:** split BTD workflow into two separate workflows (security)
  ([99ad127][78])
- **contributing.md:** split pipeline architecture information off into workflow
  README.md ([6d52302][79])
- **package.json:** ensure hidden dirs' markdown files are seen by remark
  (linted and formatted) ([1f7fad4][80])
- **package.json:** update dependencies ([d328a86][81])
- **readme.md:** fix broken links ([6e7173f][82])
- **readme.md:** improvements ([23cb780][83])
- **readme.md:** include architecture description as workflow README.md
  ([1f25e5f][84])

### [1.2.23][85] (2021-03-14)

#### ⚙️ Build system

- Better documentation ([0040582][86])

### [1.2.22][87] (2021-03-12)

#### ⚙️ Build system

- Update dependencies and fix find-package-json usage ([df9ede3][88])

### [1.2.21][89] (2021-03-12)

#### ⚙️ Build system

- **build-test-deploy.yml:** actions version updates ([29aa25a][90])
- **build-test-deploy.yml:** rollback some pipeline version updates
  ([8065757][91])
- **package.json:** fix typedoc-markdown-plugin patch ([dd3e7fa][92])
  <sup>closes [#126][93]</sup>

### [1.2.20][94] (2021-02-22)

#### ⚙️ Build system

- **package-lock.json:** update deps ([5a2d98f][95])

### [1.2.19][96] (2021-02-22)

#### 🪄 Fixes

- **.changelogrc.js:** fix dark magic ([b4157eb][97])
- **is-next-compat.ts:** never use console.log ([81533c8][98])
- **is-next-compat.ts:** use template string instead of literal ([3a4f0f1][99])
- **unit-index.test.ts:** 100% test coverage ([72189e8][100])

#### ⚙️ Build system

- **.eslintrc.js:** account for node 12 ([cad0fb2][101])
- **.github:** update workflows and templates ([54e51eb][102])
- Backport new webpack config ([b268534][103])
- **integration-external.test.ts:** ensure proper cwd is used for executing
  externals ([31c1d5b][104])
- **is-next-compat.ts:** use execa instead of shelljs under the hood
  ([9d12004][105])
- **package.json:** remove shelljs, update other deps ([11e192a][106])
- **package.json:** update dependencies ([9e1705b][107])
- Rename env-expect to expect-env ([035e98b][108])
- **setup.ts:** fix several lib-pkg tools ([44d1967][109])
- Spellcheck-commit and .changelogrc no longer use shelljs ([dd72fd1][110])
- **test:** update with new lib-pkg tools ([004a657][111])
- **unit-external.test.ts:** update with new lib-pkg tools ([6df7e73][112])

#### 🔥 Reverted

- _"debug(build-test-deploy.yml): disable debug mode"_ ([6cefa7a][113])

### [1.2.18][114] (2021-02-11)

#### ⚙️ Build system

- **package.json:** update to proper forked dependencies ([042291d][115])

### [1.2.17][116] (2021-02-10)

#### ⚙️ Build system

- **webpack.config.js:** normalize webpack configuration across repos
  ([65f48a3][117])
- **webpack.config.js:** remove ES6 syntax from JS file ([5ed6dbd][118])

### [1.2.16][119] (2021-02-10)

#### ⚙️ Build system

- **package.json:** update dependencies ([aeef7a9][120])

### [1.2.15][121] (2021-02-08)

#### 🪄 Fixes

- **readme.md:** simplify all examples with more modern syntax; remove
  @ergodark/types ([964bc47][122])

### [1.2.14][123] (2021-02-08)

#### 🪄 Fixes

- **readme.md:** add Apollo example and additional guidance ([ed357f5][124])

### [1.2.13][125] (2021-02-05)

#### 🪄 Fixes

- **config:** use transform-rename-import when building externals
  ([d224f5e][126])
- **index.ts:** use NextApiHandler type (thanks [@janhesters][127])
  ([473ff50][128])
- **integration-webpack.test.ts:** actually call bundle in test ([f7a12de][129])
- **is-next-compat.ts:** better handling of generics ([d7bc091][130])
- Next no longer misclassified as CJS ([9ebac01][131])

#### ⚙️ Build system

- **build-test-deploy.yml:** drop support for node 10 ([6adde15][132])
- **build-test-deploy.yml:** drop support for webpack 4 ([e508c06][133])
- **build-test-deploy.yml:** remove externals exception ([5e3893a][134])
- **cleanup.yml:** fix bugs in workflow ([cbf22fd][135])
- Drop support for node 10 ([71e9103][136])
- Only silence sjx if not DEBUG ([f01ce40][137])
- **package.json:** improved build-dist ([a3526f2][138])
- **package.json:** nicer destructured vals in docs ([661e62d][139])
- **package.json:** remove extraneous module ([1f2ad6a][140])
- **package.json:** update dependencies ([c64f761][141])
- **post-release-check.yml:** add five-minute-sleep ([4a0552d][142])
- **post-release-check.yml:** more resilient post-release check ([856435f][143])
- Properly mocked unit tests for externals ([b3273df][144])
- **test:** improved testing infrastructure ([fffe02e][145])
- **types:** more precise unique-filename type ([a60793c][146])

### [1.2.12][147] (2021-01-23)

#### ⚙️ Build system

- Remove erroneous module import ([6eb2a34][148])

### [1.2.11][149] (2021-01-23)

#### ⚙️ Build system

- Backport/normalize across packages ([e589c1d][150])

### [1.2.10][151] (2021-01-22)

#### ⚙️ Build system

- Update debug statement syntax ([52a2276][152])

### [1.2.9][153] (2021-01-21)

#### ⚙️ Build system

- **.github/workflows/build-test-deploy.yml:** fix peer dependency installation
  ([12e5bbe][154])

### [1.2.8][155] (2021-01-13)

#### 🪄 Fixes

- **readme.md:** ensure quick start example is functional ([87dc31f][156])

### [1.2.7][157] (2021-01-12)

#### ⚙️ Build system

- Rebuild lockfile ([94cfa38][158])
- Update babel-plugin-transform-mjs-imports ([62089c7][159])

### [1.2.6][160] (2021-01-06)

#### ⚙️ Build system

- **package.json:** prune old deps ([2cf1d29][161])

### [1.2.5][162] (2021-01-06)

#### ⚙️ Build system

- **.github/workflows/post-release-check.yml:** add new post-release-check
  ([a307efc][163])
- **.github:** add is-next-compat workflow ([1823c05][164])

### [1.2.4][165] (2021-01-06)

#### ⚙️ Build system

- **readme.md:** add quick start example ([4e5e12c][166])

### [1.2.3][167] (2021-01-05)

#### ⚙️ Build system

- **package.json:** favor "prepare" over "postinstall" and use npx for dev tools
  ([a111c87][168])

### [1.2.2][169] (2021-01-05)

#### ⚙️ Build system

- **readme.md:** cosmetic ([98b65c6][170])

### [1.2.1][171] (2021-01-05)

#### ⚙️ Build system

- **package.json:** update dependencies, prune unused dependencies
  ([6ef6cbe][172])

## [1.2.0][173] (2021-01-05)

#### ✨ Features

- **.changelogrc.js:** transfer repository over to semantic-release CI/CD
  ([b9d2bf0][174])

#### ⚙️ Build system

- **deps:** bump node-notifier from 8.0.0 to 8.0.1 ([45a79d4][175])
- **test/unit-externals.test.ts:** add mongo uri env var to test explicitly
  ([e0e1fd9][176])

### [1.1.3][177] (2020-12-06)

#### ⚙️ Build system

- **package.json:** audit and update deps ([c82695a][178])
- **package.json:** manually bump version ([813b21a][179])

### [1.1.2][180] (2020-11-26)

#### 🪄 Fixes

- **readme:** update install language ([b68c721][181])

### [1.1.1][182] (2020-11-26)

#### 🪄 Fixes

- **externals:** revert sort-package-json to maintainer version ([750055b][183])
- **externals:** rewrite test workflow ([d604dfc][184])

## [1.1.0][185] (2020-11-25)

#### 🪄 Fixes

- **build:** move Next.js dependency to peer/dev dependencies ([0e7541f][186])
- **externals:** updated remaining dependency references to peerDependency
  references ([ccf54fb][187])

### [1.0.10][188] (2020-10-24)

### [1.0.9][189] (2020-10-23)

### [1.0.8][190] (2020-10-20)

### [1.0.7][191] (2020-10-19)

### [1.0.6][192] (2020-10-17)

### [1.0.5][193] (2020-10-13)

### [1.0.4][194] (2020-10-12)

### [1.0.3][195] (2020-10-12)

### [1.0.2][196] (2020-10-07)

### [1.0.1][197] (2020-10-07)

## 1.0.0 (2020-10-07)

[1]:
  https://github.com/Xunnamius/next-test-api-route-handler/compare/v3.1.0...v3.1.1
[2]:
  https://github.com/Xunnamius/next-test-api-route-handler/commit/484d7023539d95b8930d1665b4b613042b21fe9f
[3]: https://github.com/Xunnamius/next-test-api-route-handler/issues/487
[4]:
  https://github.com/Xunnamius/next-test-api-route-handler/commit/77ad96dc4a1e3c79f9f75b6827f74f501cce8f5d
[5]:
  https://github.com/Xunnamius/next-test-api-route-handler/compare/v3.0.3...v3.1.0
[6]:
  https://github.com/Xunnamius/next-test-api-route-handler/commit/21b4b928a40b685a99df34ad20845c97615ee1c8
[7]:
  https://github.com/Xunnamius/next-test-api-route-handler/commit/2a2f0b28b07f8a176a5333551b5788033f90274a
[8]:
  https://github.com/Xunnamius/next-test-api-route-handler/commit/0ee4ce58b1c7a8b4ea2096c01142097f427b2a00
[9]:
  https://github.com/Xunnamius/next-test-api-route-handler/compare/v3.0.2...v3.0.3
[10]:
  https://github.com/Xunnamius/next-test-api-route-handler/commit/1e8cd8573cdcfa3489526244c40f373a71d92b40
[11]:
  https://github.com/Xunnamius/next-test-api-route-handler/compare/v3.0.1...v3.0.2
[12]:
  https://github.com/Xunnamius/next-test-api-route-handler/commit/84f74f55027cd4e67b7e7929f668d4de387dc3c3
[13]:
  https://github.com/Xunnamius/next-test-api-route-handler/compare/v3.0.0...v3.0.1
[14]:
  https://github.com/Xunnamius/next-test-api-route-handler/commit/a925da287a02b6c36b588b6804e7b0b628364b25
[15]:
  https://github.com/Xunnamius/next-test-api-route-handler/compare/v2.3.4...v3.0.0
[16]:
  https://github.com/Xunnamius/next-test-api-route-handler/commit/d3c60cbd506eb22a4bb23554b06668076e687ad9
[17]:
  https://github.com/Xunnamius/next-test-api-route-handler/commit/68d30dac2210e4f976afbf5c59378d6b314d4ec3
[18]:
  https://github.com/Xunnamius/next-test-api-route-handler/commit/15c899a98423c612571886115308e68e20633a1b
[19]:
  https://github.com/Xunnamius/next-test-api-route-handler/commit/5a1a2ee806f4cfd5d199d54dbd82f9f945da1694
[20]:
  https://github.com/Xunnamius/next-test-api-route-handler/commit/73f44b78c2ee92b443adf99e248c03b985b80891
[21]:
  https://github.com/Xunnamius/next-test-api-route-handler/compare/v2.3.3...v2.3.4
[22]:
  https://github.com/Xunnamius/next-test-api-route-handler/commit/854704ba9a7f374753e1a51f4fe00db761d7718f
[23]:
  https://github.com/Xunnamius/next-test-api-route-handler/commit/9302bcc882e9cd4080526f5192186b5259e08726
[24]:
  https://github.com/Xunnamius/next-test-api-route-handler/compare/v2.3.2...v2.3.3
[25]:
  https://github.com/Xunnamius/next-test-api-route-handler/commit/597c2497a137c86696aba9b750b60f43d728495f
[26]:
  https://github.com/Xunnamius/next-test-api-route-handler/compare/v2.3.1...v2.3.2
[27]:
  https://github.com/Xunnamius/next-test-api-route-handler/commit/32eafabd592856a7ef286d7d0157e38a8275695d
[28]:
  https://github.com/Xunnamius/next-test-api-route-handler/commit/cd98aab7eea7bdd4b988402b57ce5e93572a7850
[29]:
  https://github.com/Xunnamius/next-test-api-route-handler/compare/v2.3.0...v2.3.1
[30]:
  https://github.com/Xunnamius/next-test-api-route-handler/commit/91f08d426081afc1009e50d7b9ee6a0a2259268b
[31]:
  https://github.com/Xunnamius/next-test-api-route-handler/compare/v2.2.1...v2.3.0
[32]:
  https://github.com/Xunnamius/next-test-api-route-handler/commit/cd3cd95adb536b05a3cfe8bd0b12329c9acad166
[33]: https://github.com/Xunnamius/next-test-api-route-handler/issues/373
[34]:
  https://github.com/Xunnamius/next-test-api-route-handler/commit/8746e5fb6b337131303ad0c011c864d5152a864d
[35]:
  https://github.com/Xunnamius/next-test-api-route-handler/commit/ae778d18f1c01e36070f0612067ec9f00f14a665
[36]: https://github.com/Xunnamius/next-test-api-route-handler/issues/378
[37]:
  https://github.com/Xunnamius/next-test-api-route-handler/commit/c216caa659a0fcf807ff6b1a0c11c2b331e27d3c
[38]:
  https://github.com/Xunnamius/next-test-api-route-handler/commit/5fbb6d20cab097250cb8c62d0c5edb6fe80f0bfc
[39]:
  https://github.com/Xunnamius/next-test-api-route-handler/commit/346e8de1390ba46e9dc8faccc0977c5f50a9dc32
[40]:
  https://github.com/Xunnamius/next-test-api-route-handler/commit/812e6f262726e328a57cdb0833fb8bfbbcce6708
[41]:
  https://github.com/Xunnamius/next-test-api-route-handler/commit/5034aba01f30bfb7787247054d12d7dbb90469e6
[42]:
  https://github.com/Xunnamius/next-test-api-route-handler/compare/v2.2.0...v2.2.1
[43]:
  https://github.com/Xunnamius/next-test-api-route-handler/commit/de9ee177491855eb0ac095f9a1a3e5cfad820420
[44]:
  https://github.com/Xunnamius/next-test-api-route-handler/compare/v2.1.3...v2.2.0
[45]:
  https://github.com/Xunnamius/next-test-api-route-handler/commit/419d5fe805928605b85fe0e5c64c80eb5a1d798d
[46]:
  https://github.com/Xunnamius/next-test-api-route-handler/compare/v2.1.2...v2.1.3
[47]:
  https://github.com/Xunnamius/next-test-api-route-handler/commit/7916f0026b59e6325b59395f61b142056c6c8220
[48]:
  https://github.com/Xunnamius/next-test-api-route-handler/compare/v2.1.1...v2.1.2
[49]:
  https://github.com/Xunnamius/next-test-api-route-handler/commit/74241eeee173a6cf8f987608946c3d8691a67c27
[50]:
  https://github.com/Xunnamius/next-test-api-route-handler/commit/33b6a34a126909a354a7c3f5d523b0fa47acb960
[51]:
  https://github.com/Xunnamius/next-test-api-route-handler/commit/1c3425caf7d80793a2c1e88ff8fbd29ada8adf2d
[52]:
  https://github.com/Xunnamius/next-test-api-route-handler/compare/v2.1.0...v2.1.1
[53]:
  https://github.com/Xunnamius/next-test-api-route-handler/commit/fd787ca116c3a84f9393f22bf7e898db0a22f5e1
[54]:
  https://github.com/Xunnamius/next-test-api-route-handler/commit/87ed12b68e930342649c65a76455396879658d48
[55]:
  https://github.com/Xunnamius/next-test-api-route-handler/compare/v2.0.2...v2.1.0
[56]:
  https://github.com/Xunnamius/next-test-api-route-handler/commit/c51cf0222e17066c03cd80e1c76c5e9f49cacc2e
[57]: https://github.com/Xunnamius/next-test-api-route-handler/issues/295
[58]:
  https://github.com/Xunnamius/next-test-api-route-handler/commit/2b14d8499f4845d0e2d20fd2098f509f5edc16f9
[59]:
  https://github.com/Xunnamius/next-test-api-route-handler/commit/f4772607ebb8641ea4e0d6ac2fd152f76dff3f7c
[60]:
  https://github.com/Xunnamius/next-test-api-route-handler/commit/f61fd8c5ea52265a7ff15252d720d135890880f2
[61]: https://github.com/Xunnamius/next-test-api-route-handler/issues/296
[62]:
  https://github.com/Xunnamius/next-test-api-route-handler/compare/v2.0.1...v2.0.2
[63]:
  https://github.com/Xunnamius/next-test-api-route-handler/commit/fd53fefc6d5c2ff67ed2669b18e28b7ef7005c12
[64]:
  https://github.com/Xunnamius/next-test-api-route-handler/commit/e5c6a994d4b553369ae42b6be0ae1932346ebbd6
[65]:
  https://github.com/Xunnamius/next-test-api-route-handler/compare/v2.0.0...v2.0.1
[66]:
  https://github.com/Xunnamius/next-test-api-route-handler/commit/ef32668428df303c4e536aae5793ed14eee0ade5
[67]:
  https://github.com/Xunnamius/next-test-api-route-handler/compare/v1.2.24...v2.0.0
[68]:
  https://github.com/Xunnamius/next-test-api-route-handler/commit/ee31fa8cefdc2b8b8197d3889fb8aac27467b374
[69]:
  https://github.com/Xunnamius/next-test-api-route-handler/commit/2f1125cfb481e94af4248cf5b5dfce729cc4d662
[70]:
  https://github.com/Xunnamius/next-test-api-route-handler/commit/75832099f4c4d0e329aca469ac16c8a25100c26d
[71]:
  https://github.com/Xunnamius/next-test-api-route-handler/commit/bc5e72d9d40f1991315ac0657a4b212331dc065f
[72]:
  https://github.com/Xunnamius/next-test-api-route-handler/commit/bc7eb3db18aa70345a1c11d96436b374a15c3b7f
[73]:
  https://github.com/Xunnamius/next-test-api-route-handler/commit/20ca255e01d0c2e7824707e19f41ca5a8de0140e
[74]:
  https://github.com/Xunnamius/next-test-api-route-handler/compare/v1.2.23...v1.2.24
[75]:
  https://github.com/Xunnamius/next-test-api-route-handler/commit/af177c5035c22ab923dd62f6dc82702373f740d4
[76]:
  https://github.com/Xunnamius/next-test-api-route-handler/commit/364549e2845965954af62fdfa6c1dfa0d6f91f2f
[77]:
  https://github.com/Xunnamius/next-test-api-route-handler/commit/4db5d04d6a7117fe8e2113d2fafc6150a81f611c
[78]:
  https://github.com/Xunnamius/next-test-api-route-handler/commit/99ad1276e7e69218719ee2b27173e4ffcb7337f6
[79]:
  https://github.com/Xunnamius/next-test-api-route-handler/commit/6d523027b8d650ae0a2d121c349e6a4c48af6792
[80]:
  https://github.com/Xunnamius/next-test-api-route-handler/commit/1f7fad4d512f1839d96c6264f2d4abb1c5ed11e7
[81]:
  https://github.com/Xunnamius/next-test-api-route-handler/commit/d328a86317c60206bda565ba2e315113dadd0c9b
[82]:
  https://github.com/Xunnamius/next-test-api-route-handler/commit/6e7173fca4cbe778419eeff92ddbf7c03c2b00d5
[83]:
  https://github.com/Xunnamius/next-test-api-route-handler/commit/23cb7804d5f0e775b75eaefb4588beb179dcdcdf
[84]:
  https://github.com/Xunnamius/next-test-api-route-handler/commit/1f25e5fb8b2797621d316e18b01ee503fb4d1263
[85]:
  https://github.com/Xunnamius/next-test-api-route-handler/compare/v1.2.22...v1.2.23
[86]:
  https://github.com/Xunnamius/next-test-api-route-handler/commit/0040582d2f89e9a14c2335dc85cd5f9201bff644
[87]:
  https://github.com/Xunnamius/next-test-api-route-handler/compare/v1.2.21...v1.2.22
[88]:
  https://github.com/Xunnamius/next-test-api-route-handler/commit/df9ede3ddde3a2df6a42224ab3302e599bd61516
[89]:
  https://github.com/Xunnamius/next-test-api-route-handler/compare/v1.2.20...v1.2.21
[90]:
  https://github.com/Xunnamius/next-test-api-route-handler/commit/29aa25a9e2572be5b418fbee9d2d8aba2056583e
[91]:
  https://github.com/Xunnamius/next-test-api-route-handler/commit/806575792fe9e1522bd6bce0eb10f1bd3407da64
[92]:
  https://github.com/Xunnamius/next-test-api-route-handler/commit/dd3e7faadf148b23994f443a2247cc1316639e7d
[93]: https://github.com/Xunnamius/next-test-api-route-handler/issues/126
[94]:
  https://github.com/Xunnamius/next-test-api-route-handler/compare/v1.2.19...v1.2.20
[95]:
  https://github.com/Xunnamius/next-test-api-route-handler/commit/5a2d98f3ddb34e9d934f16510a73cacd43ee42ee
[96]:
  https://github.com/Xunnamius/next-test-api-route-handler/compare/v1.2.18...v1.2.19
[97]:
  https://github.com/Xunnamius/next-test-api-route-handler/commit/b4157eba128f6a787531fdabf2bebf78851a0d9a
[98]:
  https://github.com/Xunnamius/next-test-api-route-handler/commit/81533c8953adde75499cd11b552bca5f970addca
[99]:
  https://github.com/Xunnamius/next-test-api-route-handler/commit/3a4f0f150779a226ee3c9f45fde201391fa1bec0
[100]:
  https://github.com/Xunnamius/next-test-api-route-handler/commit/72189e80136b0567de8fc65eed9b2a4be365ca1a
[101]:
  https://github.com/Xunnamius/next-test-api-route-handler/commit/cad0fb2b6153434d3be41f394f1fa636cc930435
[102]:
  https://github.com/Xunnamius/next-test-api-route-handler/commit/54e51ebd0e133fb469306b76bc756c283a71a2c1
[103]:
  https://github.com/Xunnamius/next-test-api-route-handler/commit/b2685345493165cc63136b051cc5fafbf02f5c48
[104]:
  https://github.com/Xunnamius/next-test-api-route-handler/commit/31c1d5b358df78e0f27e881c0329355d91370995
[105]:
  https://github.com/Xunnamius/next-test-api-route-handler/commit/9d12004ad5adfc5d4d6992bdb67c52168829967e
[106]:
  https://github.com/Xunnamius/next-test-api-route-handler/commit/11e192a670c5cf40faff32abeecb610534cd382b
[107]:
  https://github.com/Xunnamius/next-test-api-route-handler/commit/9e1705b88fbcb5c4794abfb56691bdea7500db0d
[108]:
  https://github.com/Xunnamius/next-test-api-route-handler/commit/035e98bbe4b6bcf1ec6de40ee38b36ec107e8186
[109]:
  https://github.com/Xunnamius/next-test-api-route-handler/commit/44d1967a412ca67829deeb29c7603ddf7e42f435
[110]:
  https://github.com/Xunnamius/next-test-api-route-handler/commit/dd72fd1859fd74df3af0d47a1747d8c404abc3a7
[111]:
  https://github.com/Xunnamius/next-test-api-route-handler/commit/004a657bafaab0419e645b6388c7536e38a1ef22
[112]:
  https://github.com/Xunnamius/next-test-api-route-handler/commit/6df7e73fff51036c63efc7ba898c3d76bc47deb7
[113]:
  https://github.com/Xunnamius/next-test-api-route-handler/commit/6cefa7ae41832e61ef6df75409be61141f7d1687
[114]:
  https://github.com/Xunnamius/next-test-api-route-handler/compare/v1.2.17...v1.2.18
[115]:
  https://github.com/Xunnamius/next-test-api-route-handler/commit/042291d26742dfdda3742e6171efa25e9d3953ce
[116]:
  https://github.com/Xunnamius/next-test-api-route-handler/compare/v1.2.16...v1.2.17
[117]:
  https://github.com/Xunnamius/next-test-api-route-handler/commit/65f48a3d97184bb8a1be4fd27e86be0d7cd6bb00
[118]:
  https://github.com/Xunnamius/next-test-api-route-handler/commit/5ed6dbd1cdcb15745f4979f1a716d9bce9a93afb
[119]:
  https://github.com/Xunnamius/next-test-api-route-handler/compare/v1.2.15...v1.2.16
[120]:
  https://github.com/Xunnamius/next-test-api-route-handler/commit/aeef7a9726934852e1a51c9da98c4a96a9c70044
[121]:
  https://github.com/Xunnamius/next-test-api-route-handler/compare/v1.2.14...v1.2.15
[122]:
  https://github.com/Xunnamius/next-test-api-route-handler/commit/964bc47f80691e83d92082fcaa0679219b8543f5
[123]:
  https://github.com/Xunnamius/next-test-api-route-handler/compare/v1.2.13...v1.2.14
[124]:
  https://github.com/Xunnamius/next-test-api-route-handler/commit/ed357f5211a49bfffbb28f03d60f157fa23d14b4
[125]:
  https://github.com/Xunnamius/next-test-api-route-handler/compare/v1.2.12...v1.2.13
[126]:
  https://github.com/Xunnamius/next-test-api-route-handler/commit/d224f5eff5a786b96614b2c3f826eba610027da0
[127]: https://github.com/janhesters
[128]:
  https://github.com/Xunnamius/next-test-api-route-handler/commit/473ff500fb2c954ce32be911bde943259ae1bbef
[129]:
  https://github.com/Xunnamius/next-test-api-route-handler/commit/f7a12ded8f43359fd3079ea8294a2199c34b2d26
[130]:
  https://github.com/Xunnamius/next-test-api-route-handler/commit/d7bc091fe8f8e85b70987cfa4c663c7c8fd018c8
[131]:
  https://github.com/Xunnamius/next-test-api-route-handler/commit/9ebac018798ac82b97b8163bc5713b43001f592c
[132]:
  https://github.com/Xunnamius/next-test-api-route-handler/commit/6adde1576f4aeb8b9a72cdcefc2ea6bd4b71a5cd
[133]:
  https://github.com/Xunnamius/next-test-api-route-handler/commit/e508c06b77d225f150ebfce6409c2506a88efe4c
[134]:
  https://github.com/Xunnamius/next-test-api-route-handler/commit/5e3893a425b95ac2b12edc2195171de85afcfd0a
[135]:
  https://github.com/Xunnamius/next-test-api-route-handler/commit/cbf22fdd78e28e02ec4213156c6c72ba16c8bfa3
[136]:
  https://github.com/Xunnamius/next-test-api-route-handler/commit/71e9103df5660fea2af3211b1d6c1fa72b1dd3c7
[137]:
  https://github.com/Xunnamius/next-test-api-route-handler/commit/f01ce4041b2fb1fd24052ce17008df9746652730
[138]:
  https://github.com/Xunnamius/next-test-api-route-handler/commit/a3526f28057201fcce19c752e554e705b8e3a922
[139]:
  https://github.com/Xunnamius/next-test-api-route-handler/commit/661e62d53be74211d3d158ad90c196f43c8fe6db
[140]:
  https://github.com/Xunnamius/next-test-api-route-handler/commit/1f2ad6a2cdc863b183ac7f7bef756dd90c057ebe
[141]:
  https://github.com/Xunnamius/next-test-api-route-handler/commit/c64f761c3b2cc69cf07cd7dd88e9671deb66fc4f
[142]:
  https://github.com/Xunnamius/next-test-api-route-handler/commit/4a0552d2c730842371325111276c58651dabc558
[143]:
  https://github.com/Xunnamius/next-test-api-route-handler/commit/856435f02ebe2f44b13c92cc6c794eeab2b345d0
[144]:
  https://github.com/Xunnamius/next-test-api-route-handler/commit/b3273dfbe43cb4c9ececdb4863ff4259f38807ec
[145]:
  https://github.com/Xunnamius/next-test-api-route-handler/commit/fffe02e14615daba1f9f8ec1bb2a4024ceb93e84
[146]:
  https://github.com/Xunnamius/next-test-api-route-handler/commit/a60793c620fe926308f8c99c61076da81aebe2fa
[147]:
  https://github.com/Xunnamius/next-test-api-route-handler/compare/v1.2.11...v1.2.12
[148]:
  https://github.com/Xunnamius/next-test-api-route-handler/commit/6eb2a348b1352e9f30d7ecacbaba01fa11cf1cfe
[149]:
  https://github.com/Xunnamius/next-test-api-route-handler/compare/v1.2.10...v1.2.11
[150]:
  https://github.com/Xunnamius/next-test-api-route-handler/commit/e589c1d48aa1dae40643385c6acfcbacf9b40e16
[151]:
  https://github.com/Xunnamius/next-test-api-route-handler/compare/v1.2.9...v1.2.10
[152]:
  https://github.com/Xunnamius/next-test-api-route-handler/commit/52a22765e17759271e7ba6c83ce9f3609500b5f3
[153]:
  https://github.com/Xunnamius/next-test-api-route-handler/compare/v1.2.8...v1.2.9
[154]:
  https://github.com/Xunnamius/next-test-api-route-handler/commit/12e5bbe1bf36fda3ef938c7ed7cd445fec3901c9
[155]:
  https://github.com/Xunnamius/next-test-api-route-handler/compare/v1.2.7...v1.2.8
[156]:
  https://github.com/Xunnamius/next-test-api-route-handler/commit/87dc31f264682d8048ee8d4cba4dbf866666bf07
[157]:
  https://github.com/Xunnamius/next-test-api-route-handler/compare/v1.2.6...v1.2.7
[158]:
  https://github.com/Xunnamius/next-test-api-route-handler/commit/94cfa3806bfa0250e9b2dd5b3abfb2ff65c77c6a
[159]:
  https://github.com/Xunnamius/next-test-api-route-handler/commit/62089c79f6c9b585d2bb8ca0a8b87bd355b8695f
[160]:
  https://github.com/Xunnamius/next-test-api-route-handler/compare/v1.2.5...v1.2.6
[161]:
  https://github.com/Xunnamius/next-test-api-route-handler/commit/2cf1d29159fb746dc4a7c09a8193e46c6bec3823
[162]:
  https://github.com/Xunnamius/next-test-api-route-handler/compare/v1.2.4...v1.2.5
[163]:
  https://github.com/Xunnamius/next-test-api-route-handler/commit/a307efcf2cdf60679d68fab385bdc8951a476ace
[164]:
  https://github.com/Xunnamius/next-test-api-route-handler/commit/1823c055f034e528337c68d710164097e423f6e2
[165]:
  https://github.com/Xunnamius/next-test-api-route-handler/compare/v1.2.3...v1.2.4
[166]:
  https://github.com/Xunnamius/next-test-api-route-handler/commit/4e5e12c0df4fc80abb696d32718440ff294902e7
[167]:
  https://github.com/Xunnamius/next-test-api-route-handler/compare/v1.2.2...v1.2.3
[168]:
  https://github.com/Xunnamius/next-test-api-route-handler/commit/a111c87ccd863ce4dac85a5bd0281d87affe3b63
[169]:
  https://github.com/Xunnamius/next-test-api-route-handler/compare/v1.2.1...v1.2.2
[170]:
  https://github.com/Xunnamius/next-test-api-route-handler/commit/98b65c6da330040e4bcbc22fe28db87c3965fd0e
[171]:
  https://github.com/Xunnamius/next-test-api-route-handler/compare/v1.2.0...v1.2.1
[172]:
  https://github.com/Xunnamius/next-test-api-route-handler/commit/6ef6cbeb143648eb1fed5eff39071a06e7354275
[173]:
  https://github.com/Xunnamius/next-test-api-route-handler/compare/v1.1.3...v1.2.0
[174]:
  https://github.com/Xunnamius/next-test-api-route-handler/commit/b9d2bf010fba4b163e1eea0801271292a0e74308
[175]:
  https://github.com/Xunnamius/next-test-api-route-handler/commit/45a79d41835b5146912511f8b583c9128d154cf9
[176]:
  https://github.com/Xunnamius/next-test-api-route-handler/commit/e0e1fd951fbe63c04c264ad11ab1fa7a39e1679a
[177]:
  https://github.com/Xunnamius/next-test-api-route-handler/compare/v1.1.2...v1.1.3
[178]:
  https://github.com/Xunnamius/next-test-api-route-handler/commit/c82695a8816b6cd5f0e11d09cc2f948a30a416e9
[179]:
  https://github.com/Xunnamius/next-test-api-route-handler/commit/813b21ad1e2c78594903b3a8f504f4460d8e506e
[180]:
  https://github.com/Xunnamius/next-test-api-route-handler/compare/v1.1.1...v1.1.2
[181]:
  https://github.com/Xunnamius/next-test-api-route-handler/commit/b68c721e5100baa883c7096e5cc4e81c1c60ed00
[182]:
  https://github.com/Xunnamius/next-test-api-route-handler/compare/v1.1.0...v1.1.1
[183]:
  https://github.com/Xunnamius/next-test-api-route-handler/commit/750055b92699fc7f1c06349ccdb0ddc0179f891a
[184]:
  https://github.com/Xunnamius/next-test-api-route-handler/commit/d604dfc39d2e77cbe1234b8349a2ecef81a9e54a
[185]:
  https://github.com/Xunnamius/next-test-api-route-handler/compare/v1.0.10...v1.1.0
[186]:
  https://github.com/Xunnamius/next-test-api-route-handler/commit/0e7541fbecd2e3bacc124f624bfca2b56ceeb89f
[187]:
  https://github.com/Xunnamius/next-test-api-route-handler/commit/ccf54fb480e35961647900d345149d3cd1cf60d8
[188]:
  https://github.com/Xunnamius/next-test-api-route-handler/compare/v1.0.9...v1.0.10
[189]:
  https://github.com/Xunnamius/next-test-api-route-handler/compare/v1.0.8...v1.0.9
[190]:
  https://github.com/Xunnamius/next-test-api-route-handler/compare/v1.0.7...v1.0.8
[191]:
  https://github.com/Xunnamius/next-test-api-route-handler/compare/v1.0.6...v1.0.7
[192]:
  https://github.com/Xunnamius/next-test-api-route-handler/compare/v1.0.5...v1.0.6
[193]:
  https://github.com/Xunnamius/next-test-api-route-handler/compare/v1.0.4...v1.0.5
[194]:
  https://github.com/Xunnamius/next-test-api-route-handler/compare/v1.0.3...v1.0.4
[195]:
  https://github.com/Xunnamius/next-test-api-route-handler/compare/1.0.2...v1.0.3
[196]:
  https://github.com/Xunnamius/next-test-api-route-handler/compare/1.0.1...1.0.2
[197]:
  https://github.com/Xunnamius/next-test-api-route-handler/compare/1.0.0...1.0.1
[198]: https://conventionalcommits.org
[199]: https://semver.org
[200]:
  https://github.com/Xunnamius/next-test-api-route-handler/compare/v3.1.1...v4.0.0-canary.1
[201]:
  https://github.com/Xunnamius/next-test-api-route-handler/commit/bd552b8573c576bc8ac850f387d22ac41c64f3a2
[202]:
  https://github.com/Xunnamius/next-test-api-route-handler/commit/a1b4c9315b91eefbf3db4f209215d63c2abf8fa0
[203]:
  https://github.com/Xunnamius/next-test-api-route-handler/commit/e999cad17587f85fe4700c47b2a23753ba49a91d
