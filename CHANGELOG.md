# Changelog

All notable changes to this project will be documented in this file. See [standard-version](https://github.com/conventional-changelog/standard-version) for commit guidelines.

## [9.0.0](https://github.com/gemini-testing/testplane/compare/v8.13.2...v9.0.0) (2024-07-03)


### Bug Fixes

* Update CONTRIBUTING.md ([d569957](https://github.com/gemini-testing/testplane/commit/d56995703789bb91cb3bb80b3fe2c11a8181ed67))
* Update publish.yml ([82af530](https://github.com/gemini-testing/testplane/commit/82af5301ead43759926260793d83c8fa8926e3c6))

### [8.13.2](https://github.com/gemini-testing/testplane/compare/v8.13.1...v8.13.2) (2024-07-02)

### 8.13.1 (2024-07-02)


### ⚠ BREAKING CHANGES

* node versions less than 18.0.0 are no longer supported
* "headers" in the config are now an object with a "X-Request-ID" by default
* assertView now disables animations by default
* - tests in chrome@93 and higher now run in as isolated environment by default
* package exports have changed
* - test.id() -> test.id
- suite.id() -> suite.id
* terminate tests execution on unhandled rejections
* node versions less than 16.0.0 are no longer supported
* node versions less than 14.0.0 are no longer supported
* - change default value for "saveHistory" option from "false" to "true"
- change default value for "antialiasingTolerance" option from "0" to "4"
- change default value for "compositeImage" option from "false" to "true"
- change default value for "takeScreenshotOnFails.assertViewFail" option from "false" to "true"
- change default value for "takeScreenshotOnFailsMode" option from "viewport" to "fullpage"
- change default value for "httpTimeout" option from "90000" to "30000"
- change default value for "pageLoadTimeout" option from "300000" to " 20000"
- change default value for "sessionQuitTimeout" option from "90000" to "5000"
- change default value for "takeScreenshotOnFailsTimeout" option from "90000" to "5000"
* option "-r" is no longer sets the specified reporter, now it uses for require module
* remove deprecated options: "screenshotOnReject" and "screenshotOnRejectTimeout"
* reporters specified as function and used through programmatic API must have a static create method for initialization
* "teamcity" reporter is no longer supported, use "hermione-teamcity-reporter" plugin instead
* testParserApi object passed on BEFORE_FILE_READ event is no longer an EventEmitter
* node versions less than 12.0.0 are no longer supported
* move to latest version of webdriverio (7.x) from our fork
* remove browser options: "screenshotPath", "w3cCompatible"
* option "allowViewportOverflow" now allows to overflow bottom viewport bound

- add browser option "assertViewOpts" which is used as default options inside "assertView"
- add ability to set "compositeImage"
- add ability to set "antialiasingTolerance"
- add ability to set "captureElementFromTop" in order for more precise control of capture image
- update gemini-core from 4.0.0 to 5.0.0
* 'END' event handler will not recieve tests' statistic as the first argument
* test with duplicate state names in 'assertView' calls will fail with 'AssertViewError'
* now "assertViewResults" contains image path and size instead of only path
* **node-support:** support only node>=6.4.0

### Features

* 'orientation' command waits for screen rotate ([2e23fe4](https://github.com/gemini-testing/testplane/commit/2e23fe4545957a539c5e5f15b47bbf4bf17e657c))
* ability to add test controllers on BEFORE_FILE_READ ([1c5082e](https://github.com/gemini-testing/testplane/commit/1c5082ed821f85ace3bd6b01dc4803b554402762))
* Ability to add test to current run ([#335](https://github.com/gemini-testing/testplane/issues/335)) ([33900b3](https://github.com/gemini-testing/testplane/commit/33900b329d91364dec3c18325a00c625ce377e13))
* ability to enable/disable tests in TestCollection ([cac56f7](https://github.com/gemini-testing/testplane/commit/cac56f7367344a94372ffd0246c3da6dfa855e8e))
* ability to guarantee tests order after reading ([e14faef](https://github.com/gemini-testing/testplane/commit/e14faeff014682cf2835af3b029fb8c97bf9a23d))
* ability to iterate over all root suites in test collection ([bc02934](https://github.com/gemini-testing/testplane/commit/bc02934e70a5b81b016b8f3024c1910a87c1db92))
* ability to pass TestCollection to run method ([6e8582b](https://github.com/gemini-testing/testplane/commit/6e8582b2cd0c11b54989db1148130cd7eaa2590b))
* ability to read tests in ".jsx" and ".tsx" files ([2884a7e](https://github.com/gemini-testing/testplane/commit/2884a7ef44f19575421cbd5d50c0533cd93d75e6))
* ability to restart workers after some number of tests ([4a42b0d](https://github.com/gemini-testing/testplane/commit/4a42b0d1bbea18d6263d10c7955293af3b7295d7))
* ability to restart workers on crash ([e7e08c2](https://github.com/gemini-testing/testplane/commit/e7e08c215e556ee22cd433f058ce7eced0a28335))
* Ability to run tests in different versions of browsers ([d7df135](https://github.com/gemini-testing/testplane/commit/d7df135a044ff5adea25a3542c1e0ce083e90ff5))
* ability to run tests in isolated environment ([0f12eb3](https://github.com/gemini-testing/testplane/commit/0f12eb315d624ce10981f32c3ca853ebc45ce335))
* ability to run unit tests in browser ([0e9f9ac](https://github.com/gemini-testing/testplane/commit/0e9f9accae4a0998a03dfa74377b748976620440))
* ability to scroll page by passed selector ([7307ae1](https://github.com/gemini-testing/testplane/commit/7307ae1f5d70b935524ad11a32929ab1edbeebc4))
* add 'END' event ([4491eb1](https://github.com/gemini-testing/testplane/commit/4491eb138a27268d4871f1e0b1618d7d959f0714))
* add 'HERMIONE_SETS' environment variable ([eeca127](https://github.com/gemini-testing/testplane/commit/eeca1275cf2db12b0c5443731c12695ad5e215d2))
* add 'hermioneCtx' field to the test after reading the file ([f94c91c](https://github.com/gemini-testing/testplane/commit/f94c91cdf71ff95a2602ab1da5fd245d26099abf))
* add 'ignoreElements' options to 'assertView' command ([bd10710](https://github.com/gemini-testing/testplane/commit/bd107101a43abed3b846524880760b681bc5d0c0))
* add 'pid' in which test is executed to meta info ([e530784](https://github.com/gemini-testing/testplane/commit/e530784393ea74b5f43e804d04bbdb1b1b073e8a))
* add 'screenshotDelay' option ([ced8e9f](https://github.com/gemini-testing/testplane/commit/ced8e9f4579be7a2555addd2e9b2725cc7591e19))
* add "antialiasingTolerance" option ([88d1d1c](https://github.com/gemini-testing/testplane/commit/88d1d1c84d8110a97de7c0a3e1efe7eabf1fdef4))
* add "browserWSEndpoint" to be able to change ws enpoint ([57c0a06](https://github.com/gemini-testing/testplane/commit/57c0a06422c137c4eeaf279646896a1aa1fb2629))
* add "clearSession" browser command ([7114cd5](https://github.com/gemini-testing/testplane/commit/7114cd57bcec93a9a0b4d35ae300151ef5865a07))
* add "headless" setting for the main 3 browsers ([#768](https://github.com/gemini-testing/testplane/issues/768)) ([0400c33](https://github.com/gemini-testing/testplane/commit/0400c33f502530ffa8a3c13207d75696fcff0325))
* add "jsonl" reporter ([08140fd](https://github.com/gemini-testing/testplane/commit/08140fdbc1d630e2cbfbfba16457fc813e9f1aee))
* add "startTime" field to test result in order to use in plugins ([9dfb5ed](https://github.com/gemini-testing/testplane/commit/9dfb5ed5c278dfffb6cc7e3af3f75181cf8c41b9))
* add "UPDATE_REFERENCE" event ([8c30e0f](https://github.com/gemini-testing/testplane/commit/8c30e0f8cf45ffa5e3b1e7a24da6201f59a82faf))
* add ability not to translate events via interceptors ([243aeab](https://github.com/gemini-testing/testplane/commit/243aeaba768dbbf6041250b0f7edbb42ab030e6a))
* add ability to calibrate image before capturing ([c80f6f0](https://github.com/gemini-testing/testplane/commit/c80f6f033a3225b22f161d6dd2754be69d15d5ba))
* add ability to change file extensions ([ffb5449](https://github.com/gemini-testing/testplane/commit/ffb5449aa9de1c131e1e36d712348e2a1f46c8be))
* add ability to disable animations in assertView ([fc4dbe7](https://github.com/gemini-testing/testplane/commit/fc4dbe7e40d19c978c1510f71eb2ac7fb02bbd67))
* add ability to emit test result events from plugins ([d9e2ad7](https://github.com/gemini-testing/testplane/commit/d9e2ad775caa2296ca98ba02fc22af1f042f3a1e))
* add ability to enable new Chrome headless mode ([cbc4860](https://github.com/gemini-testing/testplane/commit/cbc486079f0989bdaf75eab9802f2b60593142d2))
* add ability to exlude paths in 'readTests' ([724c7b4](https://github.com/gemini-testing/testplane/commit/724c7b4155b2c984bb9aeaf3e8c7ba4614026fc1))
* add ability to extend "hermione" global variable ([f4c0cec](https://github.com/gemini-testing/testplane/commit/f4c0cec57c107e17fae39918542df9c039216f5e))
* add ability to extend hermione.ctx typings ([540893c](https://github.com/gemini-testing/testplane/commit/540893cd3cdadcdd25cfc4d2a0b6a114a77cc164))
* add ability to redirect output of reporter to the file ([066c590](https://github.com/gemini-testing/testplane/commit/066c59072bcb086535797888018df73502486f93))
* add ability to show user log in component tests ([772cf09](https://github.com/gemini-testing/testplane/commit/772cf09b3609e3d9c3883dfe69cc4ae7649d5616))
* add ability to specify ignoreDiffPixelCount in assertView ([32242e1](https://github.com/gemini-testing/testplane/commit/32242e15d3ed84ac52a126ca93e5a1cb4a97c34c))
* add ability to specify sets in config ([b713732](https://github.com/gemini-testing/testplane/commit/b7137327db4888f013604c79442097851ab93757))
* add ability to use browser in component tests ([022e051](https://github.com/gemini-testing/testplane/commit/022e0516f7a9a21a87fb51f773bcf10a37990f6d))
* add ability to use default export in .hermione.conf file ([b4e1d6c](https://github.com/gemini-testing/testplane/commit/b4e1d6c9748c0d67381b5ac5e043a59675aaff56))
* add ability to use dev server ([daf1bb6](https://github.com/gemini-testing/testplane/commit/daf1bb6443c327d10514c7e67c75501b8beedfc4))
* add ability to use devtools procotol through cli option ([852f375](https://github.com/gemini-testing/testplane/commit/852f375f899a26cfa7e57b1bfded87a0aa8284ff))
* add ability to use expect in component tests ([f3f97a7](https://github.com/gemini-testing/testplane/commit/f3f97a741622863062b5497a95595f933229c522))
* add ability to use import and export in test files ([8bb43e7](https://github.com/gemini-testing/testplane/commit/8bb43e70a892368653189db5a53b169840838db2))
* add ability to use plugin's default export ([f1799b0](https://github.com/gemini-testing/testplane/commit/f1799b0246feae24d34c21fae226e96c534d6be5))
* add ability to use xpath selectors in "assertView" command ([d399b5f](https://github.com/gemini-testing/testplane/commit/d399b5f155fd5f877bc4f507e0a1b2efea5c250a))
* add ability to write test steps ([e7171b2](https://github.com/gemini-testing/testplane/commit/e7171b28df0bbe71e395c0c812939287e443dac9))
* add ability to write test steps ([efead66](https://github.com/gemini-testing/testplane/commit/efead668c2bf928c6423b3cac1fe76e73612777b))
* add allowViewportOverflow option to assertView ([47bfc9f](https://github.com/gemini-testing/testplane/commit/47bfc9fc3360d4ce20468b8ed73dd7c76ae73332))
* add assertView command ([49427cc](https://github.com/gemini-testing/testplane/commit/49427ccc789dda26e6fc4ae6222ed2f391ac967e))
* add basic unhandled rejection stack trace ([5b1db43](https://github.com/gemini-testing/testplane/commit/5b1db438e7bb51b375aad13f6d3c6aedcd2feca3))
* add browser option "testTimeout" ([7835aac](https://github.com/gemini-testing/testplane/commit/7835aacad700c0a6107d93e9f0cf9aa343d0ed88))
* add browser option "waitOrientationChange" ([e15b3c1](https://github.com/gemini-testing/testplane/commit/e15b3c1d260b283bb32a1e9417179550a97c3c26))
* add built-in assert library ([01ac6de](https://github.com/gemini-testing/testplane/commit/01ac6de407f6f1926e4a03ff3917a099526db978))
* add cli option "--require" to load external modules ([c93e652](https://github.com/gemini-testing/testplane/commit/c93e6521bb71aed448cb8c8737f4eecc84412723))
* add command history to error for timedout tests ([8023d48](https://github.com/gemini-testing/testplane/commit/8023d4803297304864de036c2c7bc9e3fa1e3e90))
* add common data transfer between main process and subprocess ([88011c4](https://github.com/gemini-testing/testplane/commit/88011c4a53999ee52d782ba33f07f540adc9e430))
* add debug mode ([aaa42b7](https://github.com/gemini-testing/testplane/commit/aaa42b7dc8587f8e133f09e8c4a2b264975525a2))
* add diff clusters ([1b71aae](https://github.com/gemini-testing/testplane/commit/1b71aaefa89cdc97ff60b3966d60dbec49a2b591))
* add element's assertView method ([54724f7](https://github.com/gemini-testing/testplane/commit/54724f7269835bdb18f14058159317ace1140171))
* add error snippets ([a78ba06](https://github.com/gemini-testing/testplane/commit/a78ba064dd98ce0335d5e6f7d6ac2b0746ca4ac3))
* add getConfig to the browser instance ([30f579e](https://github.com/gemini-testing/testplane/commit/30f579e0c3ee41e8be8e4be87d6e00cc7a718f9c))
* add hermione.init method ([#196](https://github.com/gemini-testing/testplane/issues/196)) ([d532886](https://github.com/gemini-testing/testplane/commit/d532886c4f8a47f5bdba8e41adea31cd71412159))
* Add hermione.only.notIn() helper ([17b4453](https://github.com/gemini-testing/testplane/commit/17b44535f7c0353a6185a3a73d17727904eea867))
* add image sizes to "assertViewResults" ([e84ce6d](https://github.com/gemini-testing/testplane/commit/e84ce6d24771dabe1b464502b83682906961a3c5))
* add logs timestamp ([3745c7d](https://github.com/gemini-testing/testplane/commit/3745c7dcc9d5bef28f317bd97bad119df4788b17))
* add method 'hermione.ctx' to tests API ([0506da6](https://github.com/gemini-testing/testplane/commit/0506da68285cc8ecfd7501786c5f7c13ce9512ba))
* add method 'isFailed' to the API ([5852b13](https://github.com/gemini-testing/testplane/commit/5852b1317cbb703555923ce461db5eb76d13c3bd))
* add method 'isWorker' to the API ([0698611](https://github.com/gemini-testing/testplane/commit/069861160800f55e41a9239514cf947c4b7a19ba))
* add method 'registerWorkers' to Runner ([139e9b8](https://github.com/gemini-testing/testplane/commit/139e9b8630e620c2bdcb3874bd29d44011c56e1d))
* add newWorkerProcess event ([#416](https://github.com/gemini-testing/testplane/issues/416)) ([3183352](https://github.com/gemini-testing/testplane/commit/3183352e6f9ebf65db0433ce9db3cab8db8330b5))
* add option 'httpTimeout' ([8b747e0](https://github.com/gemini-testing/testplane/commit/8b747e08901060b72e9b7796194c09d2e4701e46))
* add option 'pageLoadTimeout' ([7cf389b](https://github.com/gemini-testing/testplane/commit/7cf389b3a7107fa2d6fa8ddf53b9e07b94a02229))
* add option 'resetCursor' ([0e6f767](https://github.com/gemini-testing/testplane/commit/0e6f767a8fe6f2765cd42b78d927adaafbd6dac0))
* add option 'sessionQuitTimeout' ([acc93f6](https://github.com/gemini-testing/testplane/commit/acc93f6aa35843c5c36b111c2081718a91f0ed5d))
* add option 'sessionRequestTimeout' ([a15b022](https://github.com/gemini-testing/testplane/commit/a15b02279f5d9b3e97076300cac824e90f3fcfb2))
* add option "buildDiffOpts" to configure building diff image ([b83e2ba](https://github.com/gemini-testing/testplane/commit/b83e2baff06ad02b525cd6f7c3f06a8fb2486297))
* Add optional "meta" field for browser config ([3a80d66](https://github.com/gemini-testing/testplane/commit/3a80d6662e6410ed66e2d32ec66b6080379e0e82))
* add options 'loadPlugins' to the API method 'readTests' ([7a68f0a](https://github.com/gemini-testing/testplane/commit/7a68f0a6a723565a86337bd855ed029a279799c4))
* add per browser stats ([70a7b7f](https://github.com/gemini-testing/testplane/commit/70a7b7f328cd92bb831c6366f77fee08662b0a96))
* add plain reporter ([3d30df9](https://github.com/gemini-testing/testplane/commit/3d30df979747b90035b37d56399b994f41d3d4ca))
* add programmatic API ([248caf6](https://github.com/gemini-testing/testplane/commit/248caf688009d2162eb23d2c0bbcd07d46525170))
* add relativePath to refImg ([0bb23cf](https://github.com/gemini-testing/testplane/commit/0bb23cf7b05b16bc3cdcdd176be888c2fb161b04))
* add screenshotDelay option for assertView ([0907c1b](https://github.com/gemini-testing/testplane/commit/0907c1b203ea2cb63c8c0e7527208cba7d4471e7))
* add screenshotOnReject and screenshotOnRejectTimeout options ([236efaf](https://github.com/gemini-testing/testplane/commit/236efaf47a5ee6d554da369a1508a242742cf93b))
* add sortTests for TestCollection ([02f7da8](https://github.com/gemini-testing/testplane/commit/02f7da81f5fe12b7e80800e6fe6e95acec8eca65))
* add subscriptions to parser events for TestParserAPI ([1be789a](https://github.com/gemini-testing/testplane/commit/1be789ac1b275860a36ed146b957d8c3c1b37126))
* add tolerance option to assert view command ([d87acda](https://github.com/gemini-testing/testplane/commit/d87acda7fb27b42286f88befb5e1be5e56836ebe))
* add windowSize option ([a71ea86](https://github.com/gemini-testing/testplane/commit/a71ea86ca06ae88608823b7895370dbd4d43cf26))
* added 'hasBrowserVersionOverwriten' property for test ([c0280ce](https://github.com/gemini-testing/testplane/commit/c0280ce9399cf291fa3fc9eedb3968323b18d7f0))
* added types for 'prependListener' and 'emitAndWait' methods ([a7dd400](https://github.com/gemini-testing/testplane/commit/a7dd400f9b12a74cef47f09617ee80e006356562))
* added urlTimeout option to config ([82856d9](https://github.com/gemini-testing/testplane/commit/82856d9e8c930cc962818e8b2ad9cf37dc6232dd))
* AFTER_TESTS_READ event ([45c4acb](https://github.com/gemini-testing/testplane/commit/45c4acbbe78e011a42274a55eba4bfda5fec75db))
* allow override testTimeout for specific tests ([3d3e3d1](https://github.com/gemini-testing/testplane/commit/3d3e3d1524442639a0764bfb453d91b2fbc55253))
* allow to extend cli parser via CLI event ([6d5f96a](https://github.com/gemini-testing/testplane/commit/6d5f96a908a6f48edf86a461296cc9c08d17f43c))
* allow to save command history on any error ([de078a3](https://github.com/gemini-testing/testplane/commit/de078a34e81167f7a174b3f9c57b7824d696c63d))
* assert view by selectors ([b090a5f](https://github.com/gemini-testing/testplane/commit/b090a5fdb9b74b18803a8c70c7d73864bf7cc12f))
* **assert-view:** add waitForExist ([4d20b5c](https://github.com/gemini-testing/testplane/commit/4d20b5c7da1ee1c7245c7a98104f54eff5f85597))
* BEFORE_FILE_READ and AFTER_FILE_READ events ([f2a5593](https://github.com/gemini-testing/testplane/commit/f2a5593cedde036da84f9c4fdb82ec5c373ef1c1))
* bump webdriverio from 7 to 8 ([4d98965](https://github.com/gemini-testing/testplane/commit/4d9896543f33fe9917b34b1eeddf71be64d8c307))
* change options in "assertView" command ([763be83](https://github.com/gemini-testing/testplane/commit/763be839cbf6e0c5c0c2a72215fcc99c35a50409))
* **config:** add parallelLimit option ([e116e91](https://github.com/gemini-testing/testplane/commit/e116e918763179ce7883b694affe4ad58962ddc6))
* **config:** introduce shouldRerty config option ([3a99e86](https://github.com/gemini-testing/testplane/commit/3a99e865b8081bfb78b2fbce5d6eadc35de4b580))
* **ct:** support hot module replacement ([71628ce](https://github.com/gemini-testing/testplane/commit/71628ce39d7e96978c9fcbf9059f05113bf1c352))
* do not fail on first 'assertView' error ([3bd61d4](https://github.com/gemini-testing/testplane/commit/3bd61d406a159923e10461ca9171ede26ca684c3))
* do not pass browser id on file events ([e7cdb05](https://github.com/gemini-testing/testplane/commit/e7cdb050e8de0cf8d8df97d488a99b93ce2b8ffd))
* do not pass tests' statistic on 'END' event ([437aef7](https://github.com/gemini-testing/testplane/commit/437aef7de6241c57a27f3fbbfb4cd7226e5f1203))
* do not retry test failed with no ref image error ([2055f4e](https://github.com/gemini-testing/testplane/commit/2055f4eaaff8db9f6162446e3a958da4fcbfe3ef))
* do not use browserId as esmDecorator ([4d81dfb](https://github.com/gemini-testing/testplane/commit/4d81dfbe421a62cfe9a55515d55574762f962bdb))
* do not use webdriverio screenshotOnReject option ([326a8d0](https://github.com/gemini-testing/testplane/commit/326a8d0929d0ca39588a2d6e3ceeba1fa1723565))
* drop node versions less than 12 ([48fb22b](https://github.com/gemini-testing/testplane/commit/48fb22b1aad60e33e3734f76bf20b8b2a137221a))
* drop node versions less than 14 ([fad5815](https://github.com/gemini-testing/testplane/commit/fad58157fd12908195cef05d37c6c714f4f0148b))
* drop node versions less than 16 ([01d53ec](https://github.com/gemini-testing/testplane/commit/01d53ec2b89322f4f6dd78e824e13c27a693beb6))
* drop node versions less than 18 ([d05b8fa](https://github.com/gemini-testing/testplane/commit/d05b8fa48480ffa0f49012c561a1ff450b23cad1))
* drop node versions previous to 8 ([5136865](https://github.com/gemini-testing/testplane/commit/513686590f22a9dd7462e3527b4f55e74695b5a3))
* emit 'INIT' event for each worker ([f9f7f54](https://github.com/gemini-testing/testplane/commit/f9f7f5406e91fdd96504c5d783cd46411a9f8d80))
* emit BEGIN event between runners initialize and tests execution ([6e3f56b](https://github.com/gemini-testing/testplane/commit/6e3f56ba611ba5080f4fcc31eaea1debd7ffd161))
* enhance stacktraces ([36bb693](https://github.com/gemini-testing/testplane/commit/36bb693e3df7485ad1b1016d3c2f1f88560da29b))
* esm modules support ([5fc3272](https://github.com/gemini-testing/testplane/commit/5fc3272fc24da88315d0298c9212d6ed13615f61))
* export Key from webdriverio ([57e345e](https://github.com/gemini-testing/testplane/commit/57e345e006ab8318bd733ec0ea6c99a17baade4e))
* export TestCollection and Test types ([#806](https://github.com/gemini-testing/testplane/issues/806)) ([a4771a2](https://github.com/gemini-testing/testplane/commit/a4771a24fc0f10ef647b989461096b5cfe4d50ad))
* export TestError type ([#848](https://github.com/gemini-testing/testplane/issues/848)) ([f860b7c](https://github.com/gemini-testing/testplane/commit/f860b7c3a93e7c1cbac8347d63d27d64c00817ea))
* expose errors from before hook and test fn ([#328](https://github.com/gemini-testing/testplane/issues/328)) ([2dbc1b3](https://github.com/gemini-testing/testplane/commit/2dbc1b3432f7942019dbac415184457caf1e3c7c))
* extend browser config with its id ([06e85f6](https://github.com/gemini-testing/testplane/commit/06e85f69a9cb2e6c22fdfc948f71e229b8019104))
* extend test error with original selenium error ([500d30c](https://github.com/gemini-testing/testplane/commit/500d30c52c1e1bf635bd500c64892b6c6d9b5db8))
* forbid using of 'before' and 'after' hooks in tests ([0d76164](https://github.com/gemini-testing/testplane/commit/0d76164ef7746d2489e35cb983171067d8a3d2b6))
* generate "X-Request-ID" header ([35df5cc](https://github.com/gemini-testing/testplane/commit/35df5cce8b315df442753fbc739227d499378c71))
* generate "X-Request-ID" header for each browser request ([d40cd6a](https://github.com/gemini-testing/testplane/commit/d40cd6a9e9bf9182ab1552c52e0199cf8e1d00c5))
* hermione constructor can take configuration as an object ([1666a29](https://github.com/gemini-testing/testplane/commit/1666a29235ade8d3f280c76283790c2fe6de3520))
* implement 'testsPerSession' option ([a5f817e](https://github.com/gemini-testing/testplane/commit/a5f817ea235e4c76b196bc69d55d22df3cfd65c0))
* implement events interceptor API for plugins ([d8a4199](https://github.com/gemini-testing/testplane/commit/d8a4199e83a807ee711260e2f93ec49a300f83f6))
* implement REPL interface to debug tests ([8c17648](https://github.com/gemini-testing/testplane/commit/8c1764810da85258ff86dcac0d12f35b6eb7e1dc))
* Implemented browser version assert ([d496740](https://github.com/gemini-testing/testplane/commit/d49674021e38065be6d78acea7be10206d3c4b72))
* Implemented commands-history ([b4c1531](https://github.com/gemini-testing/testplane/commit/b4c1531b3ada00c3d7e0044cb93d5955a0e10553))
* introduce hermione.halt method ([ac028fe](https://github.com/gemini-testing/testplane/commit/ac028fe292164a5795fd0ca34ccc391f526d4041))
* issue templates ([7b112dc](https://github.com/gemini-testing/testplane/commit/7b112dc09f33014bda2dfe636145f49145b82ffa))
* load plugins and pass events when reading files ([b402217](https://github.com/gemini-testing/testplane/commit/b40221792782f08021bbde95f8b010ff21dc3d65))
* load plugins synchronously in constructor, add async INIT event ([128681a](https://github.com/gemini-testing/testplane/commit/128681af8e622acb2260eb680de3712617eae212))
* load test files asynchronously ([026e3d8](https://github.com/gemini-testing/testplane/commit/026e3d8f16df2d89128f6fa66c1ad9ea71cfecad))
* make browser.url work like url.resolve ([727f78d](https://github.com/gemini-testing/testplane/commit/727f78d95e957cdf89ca95e72f52cd01e300d96e))
* make hermione instance available from hermione plugins ([0767d5f](https://github.com/gemini-testing/testplane/commit/0767d5fd5fed5fae185cd2b1f9ca03b925bc5adc))
* make id a plain property ([fcdea03](https://github.com/gemini-testing/testplane/commit/fcdea03131e1c46c148e957b0f70dee8a55431df))
* merge gemini-core ([0760792](https://github.com/gemini-testing/testplane/commit/07607922d4ec81a7c73382163f013678db76c1f2))
* move from mocha@2.4.5 to @gemini-testing/mocha@9.1.5 ([c181f42](https://github.com/gemini-testing/testplane/commit/c181f423e636b27f1502ef9ed5dea778c50862e6))
* move mouse cursor to "body" coordinates 0,0 before each run test ([2c16f81](https://github.com/gemini-testing/testplane/commit/2c16f81f91d7835253927b582b300c109b8a4ef9))
* move to mocha upstream ([2b1f0ef](https://github.com/gemini-testing/testplane/commit/2b1f0efae978dcf37c896366eeb8bb3521bb4765))
* new ./bin/testplane ([#892](https://github.com/gemini-testing/testplane/issues/892)) ([dfc26e9](https://github.com/gemini-testing/testplane/commit/dfc26e998f12f84e7db37dc29af9bca24682d9e6))
* NEW_BROWSER event ([480401a](https://github.com/gemini-testing/testplane/commit/480401a6558aaf9929e2f7599481467c258387b5))
* **node-support:** drop of support node below 6.4.0 ([dae8e6c](https://github.com/gemini-testing/testplane/commit/dae8e6c509d2877b1496184f0b5f49293c82f33c))
* option '--update-refs' for 'assertView' command ([186ca73](https://github.com/gemini-testing/testplane/commit/186ca738ee8dfab340866923abf930882032846b))
* option 'compositeImage' for 'assertView' command ([610df5e](https://github.com/gemini-testing/testplane/commit/610df5e7b113ae534430f309ee1e1bd9d177be5a))
* option 'screenshotMode' ([35dd71e](https://github.com/gemini-testing/testplane/commit/35dd71e90b46a921b347aadf016aaf931677a791))
* own test runner instead of mocha for master process ([667ca48](https://github.com/gemini-testing/testplane/commit/667ca482a7bc292ea7790512106c01c785929f13))
* parse tests before runner start ([67a5ac7](https://github.com/gemini-testing/testplane/commit/67a5ac7235f2fa977516ede014dab65dd6ec2894))
* pass browser into test as an argument ([7b5d655](https://github.com/gemini-testing/testplane/commit/7b5d655402eabdbdbbd184bb0f5786d0704c86ba))
* pass diff bounds to error from looks-same ([fbb73c3](https://github.com/gemini-testing/testplane/commit/fbb73c3150cc9c884d1f97750a10665c119a66ed))
* pass mocha suite on 'beforeFileRead' and 'afterFileRead' events ([3e25894](https://github.com/gemini-testing/testplane/commit/3e25894e9b145ed23ef74ba044eb3c4b401ba615))
* provide the ability to modify retries count from plugins ([fc1a372](https://github.com/gemini-testing/testplane/commit/fc1a372e53caa02618d2f99030049954872cae7a))
* re-write major parts of hermione to typescript and get rid of typings ([c02e716](https://github.com/gemini-testing/testplane/commit/c02e716d62e3acd4537b0fb5f937b1a783c15d3d))
* read test files in master only once ([1cb6b0c](https://github.com/gemini-testing/testplane/commit/1cb6b0c1b2e1cc5ae6e91d781c201ccb801b2d09))
* read tests sequentially in worker ([78e8485](https://github.com/gemini-testing/testplane/commit/78e84854ee334242e6867dddc41bcb07a641f233))
* reject session if error matches on patterns from config ([775e0ea](https://github.com/gemini-testing/testplane/commit/775e0ea5277580ee6e211d2906b66376058e34af))
* release browser before firing any test finish event ([876510a](https://github.com/gemini-testing/testplane/commit/876510a2c046360f02eb5ea831ae64cca1e337db))
* remove backwards compatibility layer in TestCollection ([dfd9e72](https://github.com/gemini-testing/testplane/commit/dfd9e7263c70ac46df8a3e136c6aba86d8c8367d))
* remove handling of 'before*'-hooks failure in tests ([0c74de2](https://github.com/gemini-testing/testplane/commit/0c74de29ff8aab4f9f27f76a57546f085d815de5))
* remove hermione facade module ([738796b](https://github.com/gemini-testing/testplane/commit/738796b42bccdf0d48b6155a3d85812da45f3492))
* remove runnable type property ([8ad298f](https://github.com/gemini-testing/testplane/commit/8ad298fee4befdad511a46ff5fd155f32ef2a541))
* remove suite field in *_FILE_READ events ([91c0799](https://github.com/gemini-testing/testplane/commit/91c0799354e4ab254d5d38efd5f3360dd857fa05))
* reset cursor position to (0, 0) before open the url ([cab14ee](https://github.com/gemini-testing/testplane/commit/cab14eec2ed30b7199fe7930ed6f1e6faaeed068))
* reset cursor position to (0, 0) before running test ([1af4309](https://github.com/gemini-testing/testplane/commit/1af43092c394d8c105c4a409c63ecd90f1287e11))
* reset cursor position to 0, 0 before running test ([45a11e7](https://github.com/gemini-testing/testplane/commit/45a11e764a9f230ffca5602b42a27fbc5de7d50c))
* return all meta on getMeta call without arguments ([79264e2](https://github.com/gemini-testing/testplane/commit/79264e215cf5c896c45ef653d8b13a25057605d1))
* reuse session options in worker from master ([1a50a87](https://github.com/gemini-testing/testplane/commit/1a50a87196e12ba1c395527d297ebabb5fa0029f))
* run retries first ([82a08a7](https://github.com/gemini-testing/testplane/commit/82a08a77ca3a5dd225de9bce080f4382b2cf2eb4))
* run tests in isolated env in chrome@93 and higher by default ([473e96a](https://github.com/gemini-testing/testplane/commit/473e96a40537d56f14c0dffd77af0b3adb5108bc))
* running of tests in subprocesses ([fbb51f6](https://github.com/gemini-testing/testplane/commit/fbb51f6d7812548763e5a899260d18ccc8e20722))
* send session id on browser session events ([189faff](https://github.com/gemini-testing/testplane/commit/189faff2a53b4dcc8cd8620dbef7c2abd56bf89d))
* set default browser orientation before each test ([990a210](https://github.com/gemini-testing/testplane/commit/990a21093d5fd757cec84acaa34d6c649aefad7b))
* set window size from config before each test ([b4665cf](https://github.com/gemini-testing/testplane/commit/b4665cf8a0b5cfca5514835d75f1146d5e785de8))
* **sets:** add set.ignoreFiles option to ignore dirs while test finding ([53749c8](https://github.com/gemini-testing/testplane/commit/53749c8af5f0ba35586d9366410a5f51f89b3ee4))
* silently skip disabled tests ([e0c37eb](https://github.com/gemini-testing/testplane/commit/e0c37ebde2e60c21a724b50ee412d2aad5cd921f))
* **stats:** emit test statistics on RUNNER_END ([320da47](https://github.com/gemini-testing/testplane/commit/320da4773de612ff3d1df4d0dbf3a4620c24f5e7))
* Store a browser version in a meta object of a test-case ([f93e3bf](https://github.com/gemini-testing/testplane/commit/f93e3bfab1dc76ad628361cfd422311e8f351e13))
* stub browser commands in broken session ([c61c927](https://github.com/gemini-testing/testplane/commit/c61c927e14ec6f7eaf535e1c05e91b2eab77a4fc))
* SuiteCollection.eachTest method ([0871b7d](https://github.com/gemini-testing/testplane/commit/0871b7de4cb3c92ea4eeba8d097169d3325ecb9e))
* support tests and config on typescript ([c5f933d](https://github.com/gemini-testing/testplane/commit/c5f933df01cce6c88ad970fef430ad17aa411fc1))
* take screenshot on test or hook fail ([ec47808](https://github.com/gemini-testing/testplane/commit/ec478087f347b6a012a4640190fb0271c93d19fd))
* update gemini-core to the version with png-img@4 ([58f3da8](https://github.com/gemini-testing/testplane/commit/58f3da8282970b5a09b6bc9c969298d0d8313bf9))
* update lodash version to 4.x ([68500a0](https://github.com/gemini-testing/testplane/commit/68500a041d46b50dbf64026bee2e470e80523a5c))
* update looks-same ([e9ac36d](https://github.com/gemini-testing/testplane/commit/e9ac36d83250e6370b32d91b212f3b9d02404d65))
* update png-img ([01712eb](https://github.com/gemini-testing/testplane/commit/01712eb8d0da1230f541cc88fb7610c1e8804b88))
* update wdio version ([761a417](https://github.com/gemini-testing/testplane/commit/761a417cecb561e2cb704f5fddab5f4e232395e1))
* update wdio@4 to wdio@7 ([66057b4](https://github.com/gemini-testing/testplane/commit/66057b40c03d531fce555903a9ff088aac9b3e27))
* use new glob-extra version ([2e7509f](https://github.com/gemini-testing/testplane/commit/2e7509fd11ee880a5f31a277212f1993e741923f))
* use own runner instead of mocha in workers ([dad7707](https://github.com/gemini-testing/testplane/commit/dad770755a135d2608d0b7f1ea6ff1d1be8b39b2))
* use own test/suite/hook objects ([1384001](https://github.com/gemini-testing/testplane/commit/13840017d5203b43e3ae9bcb04f11e1460288680))
* use own test/suite/hook objects ([228a5c9](https://github.com/gemini-testing/testplane/commit/228a5c96205937b34086b9c835a88f0286842198))
* use ref image from looks-same ([ff4635a](https://github.com/gemini-testing/testplane/commit/ff4635a36f238a4c03550d22ac7b778a0c0d415b))
* use testplane env prefix with hermione fallback ([0aadd8f](https://github.com/gemini-testing/testplane/commit/0aadd8f126b6d34c064df19a248ecf88436b82c4))
* w3c browsers support ([49aa5dd](https://github.com/gemini-testing/testplane/commit/49aa5dd4c01d74751cc4f99bea26b340d39fcda3))
* wait for plugins load ([6499b2c](https://github.com/gemini-testing/testplane/commit/6499b2cc4a61d793f45da5ea1e2649120b050570))
* wait page load ([6908156](https://github.com/gemini-testing/testplane/commit/69081562322367cc64d6f4ab340d3d704d1af27f))
* **wdio:** update wdio version ([613d31a](https://github.com/gemini-testing/testplane/commit/613d31ac58b159346da8e4bec35475ae0669b7a7))
* wrap tests running in command ([fcbd8bf](https://github.com/gemini-testing/testplane/commit/fcbd8bf50098f351dcbf60cc729d9095a3d49a08))


### Bug Fixes

* .only does not work for all browsers ([fb855ca](https://github.com/gemini-testing/testplane/commit/fb855cac2b0ce3a98b7d3d0bdb3e3865cadebb45))
* 'global.hermione' is not defined when reading tests via 'readTests' ([64ff66a](https://github.com/gemini-testing/testplane/commit/64ff66a7cc1dbda539e3e3b6065a0f3d3e37ec24))
* 'hermione.ctx' is not available in a callback of test ([a6fec7c](https://github.com/gemini-testing/testplane/commit/a6fec7c8ac2326007b4f20b6ec36a5bb008b2f7c))
* 'hermione.only.in' functionality ([6f575c8](https://github.com/gemini-testing/testplane/commit/6f575c86709f66af27d492225dc0288870dc74f4))
* 'this' pointer in custom commands ([1a2b486](https://github.com/gemini-testing/testplane/commit/1a2b48632b406e44fe0bb1882fad1017c81717b7))
* "assertView", "moveCursorTo", "executionContext" and "currentTest" types ([bd4e898](https://github.com/gemini-testing/testplane/commit/bd4e8980fcffbad59af6df48726418586b1bae4a))
* ability to disable tests isolation ([51b87fd](https://github.com/gemini-testing/testplane/commit/51b87fd21ddfefe0ee46bb1105ee61ccc14d5d92))
* ability to load local files through cli option "require" ([cdd8772](https://github.com/gemini-testing/testplane/commit/cdd8772a00f0bed5fd6fa024ae8a0062f3a2f852))
* ability to run tests using "devtools" protocol ([85bc868](https://github.com/gemini-testing/testplane/commit/85bc8689585dc3ff55c0639653db84d176025bf8))
* add ability to specify runStep resolved value ([e7f1130](https://github.com/gemini-testing/testplane/commit/e7f113071f26b40d3f82514fbeb77c06fdca4598))
* add ability to take screenshot if element is out of the bounds ([6c55e74](https://github.com/gemini-testing/testplane/commit/6c55e74c3c38e13009aea5351dbf7af42e8b7dde))
* add backwards compatibility for hermione.readTests ([c19235f](https://github.com/gemini-testing/testplane/commit/c19235f8dc8a85b9e8db7420e06e9a40e116432f))
* add correct error handling in before and beforeEach hooks ([561342a](https://github.com/gemini-testing/testplane/commit/561342a860cb620178050f7d772c277d3e69e9e5))
* add err field to test result ([5f6dbe4](https://github.com/gemini-testing/testplane/commit/5f6dbe4811389d1da92decbbeedb5a59553b4c06))
* add error catch on set page load timeout for edge with w3c support ([f7e438b](https://github.com/gemini-testing/testplane/commit/f7e438b1318369636419bb8bf6001800846bab26))
* add getConfig command typings ([5889066](https://github.com/gemini-testing/testplane/commit/5889066aab9634f402eeb971bb908fcc5e919a08))
* add missing command types (moveCursorTo and openAndWait) ([#876](https://github.com/gemini-testing/testplane/issues/876)) ([5268a44](https://github.com/gemini-testing/testplane/commit/5268a4435a42e42b2aad4b245e8ae93a136f676f))
* add typings for "switchToRepl" and "clearSession" commands ([0e85f3b](https://github.com/gemini-testing/testplane/commit/0e85f3ba6efb00778ecccde9a17260c65a7e842a))
* add typings for overwriteCommand: custom commands ([420ec8b](https://github.com/gemini-testing/testplane/commit/420ec8bb3d86a2eac8ebb0aea6b02e592a92365b))
* afterEach hook error overwrites original test error ([d29f549](https://github.com/gemini-testing/testplane/commit/d29f549fc60b80f207106d67b5d0fed222b1327c))
* allow unknown options before parsing config file ([b79ad34](https://github.com/gemini-testing/testplane/commit/b79ad34d060d71123c6d56af17f15b30a23af090))
* always release browser ([cdbb742](https://github.com/gemini-testing/testplane/commit/cdbb742619cc8a2938826f88cb816ee92b7b4c80))
* **assert-view:** missed hermioneCtx on assertView execution ([8facf53](https://github.com/gemini-testing/testplane/commit/8facf5382689c8f2164abbb8840a2e1d62e6dce7))
* AssertViewError should not replace runtime error ([7e6aca4](https://github.com/gemini-testing/testplane/commit/7e6aca4078d4ace308900e8c0ee4573fa656b9e4))
* **attach:** pass "requestedCapabilities" in order to using CDP in CI ([dbff2a5](https://github.com/gemini-testing/testplane/commit/dbff2a5095784024f3a05e18c5d5968f76b1bd6b))
* avoid hermioneCtx sharing between different test runs ([2917922](https://github.com/gemini-testing/testplane/commit/2917922d413e7d3fe005afdbb8eb77d17d341d9d))
* Boolean env and cli vars reading ([fb5e932](https://github.com/gemini-testing/testplane/commit/fb5e9328e766e1f6e949671a8715e2df330e959d))
* browser calibration ([2391a28](https://github.com/gemini-testing/testplane/commit/2391a28b81f671b76d6a36497772b4a12df25488))
* bug with file path on 'before all' hook ([a3ffee7](https://github.com/gemini-testing/testplane/commit/a3ffee79b36e1de0a10ae64004aeaeb17777dae2))
* bug with incorrect work in internet explorer ([6c8924f](https://github.com/gemini-testing/testplane/commit/6c8924fc104a34d0c0000ef82c1d715f0385c785))
* call "getUrl" if url is not passed in "url" wrapper ([24dbd18](https://github.com/gemini-testing/testplane/commit/24dbd1877956602b4c0a324ae56ed9cb1f5ede86))
* call BrowserTestParser methods correctly in workers ([c46ba8f](https://github.com/gemini-testing/testplane/commit/c46ba8fc6cb745f7e994d2cf3371439d31ec2044))
* callback type for "it" and hooks ([57071e6](https://github.com/gemini-testing/testplane/commit/57071e66528d5cdf9f48baaff7e92ec504cd7d17))
* change error throwing on not existing element ([16dea03](https://github.com/gemini-testing/testplane/commit/16dea0320ba85c42f207c7c4cd6c0fd773897f2b))
* change some default values to more commonly used ([40b8343](https://github.com/gemini-testing/testplane/commit/40b8343393844f5e2f2eeef721d4a1b2e2d53201))
* collect correct statistics for tests run ([c0abd8d](https://github.com/gemini-testing/testplane/commit/c0abd8d86fe46bb9a5e6df2ec3b68d0f575c6c39))
* config property "shouldRetry" now works correctly ([2645612](https://github.com/gemini-testing/testplane/commit/2645612f929ca0eb5add3a5233f5a963c231d75f))
* correct documentation about compare options ([543d165](https://github.com/gemini-testing/testplane/commit/543d1655e8d7ae95923c138cadbd44f6bf4dc936))
* correct logic for running it.only/describe.only ([b448222](https://github.com/gemini-testing/testplane/commit/b44822243a45bf0e7dee01d9d8a90505d4ca607a))
* correct passing of 'screenshotOnReject' option in subprocesses ([8faae64](https://github.com/gemini-testing/testplane/commit/8faae64b424fca1c3edfd6b48a0f01109339570e))
* correct passing of errors from subprocesses to the main process ([13e4c17](https://github.com/gemini-testing/testplane/commit/13e4c171ff482bc8ba86ee89488fdc0bb1a62d94))
* correct resolving of baseUrl in config ([c010dc6](https://github.com/gemini-testing/testplane/commit/c010dc6c95152b94dced1032560d98b397f35b37))
* correct work of "patternsOnReject" ([a936006](https://github.com/gemini-testing/testplane/commit/a93600655cee3e77c658363774281d5bca6405d6))
* correctly calculate "height" in device with fractional pixel ratio ([7c2e066](https://github.com/gemini-testing/testplane/commit/7c2e066b0e9e38fc8fd5a8b30438786691c67531))
* correctly connect to vite server from clients (worker, browser) ([d77ee9d](https://github.com/gemini-testing/testplane/commit/d77ee9dbcf02ccb4c8be211afcb18dc7e4ce4ea2))
* correctly disable animations in inframes for ios ([5db5fa8](https://github.com/gemini-testing/testplane/commit/5db5fa87bec3e645204bca6bc7fbe580e0954ba6))
* correctly disable test execution timeout in repl mode ([bc91823](https://github.com/gemini-testing/testplane/commit/bc918235fb259b31d21c33cce23eae5b07119778))
* correctly generate test x request id for each test in one browser ([443056b](https://github.com/gemini-testing/testplane/commit/443056bb7f4b29b2694516d041e4c0403b9669e3))
* correctly mock "debug", "saveScreenshot" and "savePDF" ([202af7d](https://github.com/gemini-testing/testplane/commit/202af7d82f2d9741aa5b0478bc14c793974eb059))
* correctly read tsx files with types ([ac77d36](https://github.com/gemini-testing/testplane/commit/ac77d36cd44eca491b39d727a39d8159c73ac34a))
* correctly require plugins with yarn+pnp ([7708cf8](https://github.com/gemini-testing/testplane/commit/7708cf8edd5c3bacc3e27146149302afd86c7746))
* correctly screen element after moveTo ([b65169e](https://github.com/gemini-testing/testplane/commit/b65169e3219b54afa382fbe69e5dfbf02916c3cb))
* correctly screen elements inside iframes ([9ecf164](https://github.com/gemini-testing/testplane/commit/9ecf164f972b067084c1fa3d4b0d58c0dd3ee91f))
* correctly screen elements on device with fractional pixel ratio ([7b153d9](https://github.com/gemini-testing/testplane/commit/7b153d95eb9867e6340d264a048dda812e7db8fd))
* correctly specify "testplaneCtx.assertViewResults" type ([e10c718](https://github.com/gemini-testing/testplane/commit/e10c7184bbd326ca550224c7246ba3d6b3acf333))
* correctly switch between iframes on disable animation ([eabea08](https://github.com/gemini-testing/testplane/commit/eabea08feaa7bbb1b1f4e74a7a473115be72444a))
* create browser pool after emit INIT event ([4518b30](https://github.com/gemini-testing/testplane/commit/4518b305bba5c07aa7bfc07bc02b7bcd678e9d1c))
* **ct:** correctly support custom element commands ([5817e92](https://github.com/gemini-testing/testplane/commit/5817e92916be7e97940cec1940bc19296be28687))
* **ct:** do not fail on log html elements ([016dc45](https://github.com/gemini-testing/testplane/commit/016dc45ec6cb083c0c8db75192636c1795563c51))
* **ct:** generate url in format "/run-uuids/:uuid" ([dd61276](https://github.com/gemini-testing/testplane/commit/dd612765119baa97b777fad577d1b5d105e6ffff))
* **ct:** read tsx files with types ([c8fcd87](https://github.com/gemini-testing/testplane/commit/c8fcd87f45f9b4aa6b17bc51331d981f2f1e0d91))
* **ct:** use correct type for config from vite ([b152038](https://github.com/gemini-testing/testplane/commit/b15203876b8a0ca8cc323a7c242955008cb94c87))
* default options overrides options from the config ([186cb86](https://github.com/gemini-testing/testplane/commit/186cb86899bf64d34fca38456f1fdeb4613c9258))
* determine browser versions before run ([e73cce6](https://github.com/gemini-testing/testplane/commit/e73cce6830b875e400e58a558c4c0c76268e4ef3))
* **devtools:** do not use cache for browsers ([bf5afb0](https://github.com/gemini-testing/testplane/commit/bf5afb0204eb232fd9c8758b7353290c508c45ae))
* do not convert ref image file to base64 to get size ([b1b8ef8](https://github.com/gemini-testing/testplane/commit/b1b8ef82b28b6131fb02ae64a6765ff57af08c80))
* do not fall by memory in looks-same ([6f11eda](https://github.com/gemini-testing/testplane/commit/6f11eda3a7f673547d006171821120c89a34866c))
* do not fall if port is not specified in "gridUrl" ([4e6f49e](https://github.com/gemini-testing/testplane/commit/4e6f49e9a15c01a4a1196fa8138e02e668bf1e15))
* do not hang on errors in config.prepareBrowser ([643a344](https://github.com/gemini-testing/testplane/commit/643a344306a5151b1aeb6e32e2136debebbdaf22))
* do not ignore assertView errors in broken session rejection ([b65fe38](https://github.com/gemini-testing/testplane/commit/b65fe3878c43984b95e9dd63e981acf0c993ea81))
* do not lost "testXReqId" when using "parallelLimit" ([8d6d82a](https://github.com/gemini-testing/testplane/commit/8d6d82a3ff810c8be437a014f40fee7b70cddd9f))
* do not overwrite system.mochaOpts.grep property in workers ([8dce8ad](https://github.com/gemini-testing/testplane/commit/8dce8adb110fe0f960a996792bc7385b8b8d6317))
* do not pass browser to retried tests ([b2cb7cc](https://github.com/gemini-testing/testplane/commit/b2cb7cc14986692454e283934310ed2d8af0b634))
* do not passthrough parser events via TestParserApi ([5f26c80](https://github.com/gemini-testing/testplane/commit/5f26c80f519ea002780cf6b06214c79335a3bfdc))
* do not reinit cached browser session in worker ([761dcb8](https://github.com/gemini-testing/testplane/commit/761dcb897969ac45296b54dad42e0a55ab15efc8))
* do not remove spaces in runnable title ([df139ea](https://github.com/gemini-testing/testplane/commit/df139eac20ce00d4960b46c0b6ea57e7da06baf8))
* do not require .d.ts file ([#831](https://github.com/gemini-testing/testplane/issues/831)) ([91708d2](https://github.com/gemini-testing/testplane/commit/91708d2eec83c790591494706d607e1dcc8c4b77))
* do not restore existing 'global.hermione' variable ([e046226](https://github.com/gemini-testing/testplane/commit/e04622686fea0b63c2bf48ee45c9267e37af16b0))
* do not restore windowSize after its change in test ([22d4ab3](https://github.com/gemini-testing/testplane/commit/22d4ab3412f33cf7cc3dcb1ff90968c5155c9f27))
* do not retry worker init on fail ([28352cd](https://github.com/gemini-testing/testplane/commit/28352cde74ad85e92972a42402eb181404557a4e))
* do not run 'before' and 'after' hooks for a skipped suite ([2da0467](https://github.com/gemini-testing/testplane/commit/2da046706e0dd1871ab199895d5c2ee04dfc0ddd))
* Do not save whole runnable object - decrease memory leaks ([d1c0224](https://github.com/gemini-testing/testplane/commit/d1c022439f00bbe831be96d288b0f66fc8949d04))
* do not start browsers for skipped suites ([c3d6bb1](https://github.com/gemini-testing/testplane/commit/c3d6bb1bf5c0d9f7f9dfae6dec2888f4512651e0))
* do not store all mocha instances in workers ([ed7aab4](https://github.com/gemini-testing/testplane/commit/ed7aab432d71dc6275b0fd63b2edf6c6a3e9be52))
* do not swallow errors in hermione config ([e262fae](https://github.com/gemini-testing/testplane/commit/e262fae9046a67eea6431dedddd017b2a72e7d7e))
* do not wrap system commands ([47c9776](https://github.com/gemini-testing/testplane/commit/47c9776839fbe793ee7b283542ae57133f238224))
* dont remove imports in nodejs env ([f132eeb](https://github.com/gemini-testing/testplane/commit/f132eebc12d0dcd71e5897503fd5d1a1ad526c50))
* drop webdriverio command history after each test in workers ([51c4daf](https://github.com/gemini-testing/testplane/commit/51c4daf21e22487349872d5450144ff949ce9f97))
* emitting of fail event from plugin does not fail process ([45e519e](https://github.com/gemini-testing/testplane/commit/45e519e2da6a6cf08d92fa7d1c7280c1060035f9))
* empty test-collection sorting ([#403](https://github.com/gemini-testing/testplane/issues/403)) ([fb87508](https://github.com/gemini-testing/testplane/commit/fb87508ccab483e2432b575192df577394d1093f))
* error in expectation of orientation change ([3c8b21d](https://github.com/gemini-testing/testplane/commit/3c8b21d211f4a7dc3ce5d83c2088924337d5470a))
* errors in typings ([49e1117](https://github.com/gemini-testing/testplane/commit/49e1117ab921b3c3cf8eb95c5f56f4cd97813a25))
* even more proper lists ([4a078e8](https://github.com/gemini-testing/testplane/commit/4a078e8f522f755a9ac72cc045e681c50ac809b6))
* **existing-browser:** do not pass unnecessary options ([451d23a](https://github.com/gemini-testing/testplane/commit/451d23ad59f90f1cc7e112015d5f4f1d57915123))
* **existing-browser:** fix request and response custom transforming ([714ddb9](https://github.com/gemini-testing/testplane/commit/714ddb93c97c325ec7e8caca134c15da22e18fb4))
* export AssertViewOpts type ([2b1a4dd](https://github.com/gemini-testing/testplane/commit/2b1a4ddb9dbdc17e9077d3561ce1718403eded7e))
* export HermioneCtx type ([363ed89](https://github.com/gemini-testing/testplane/commit/363ed89944411c516bef42dd3f75a1863e5dc0da))
* export TestResult and Suite types ([#786](https://github.com/gemini-testing/testplane/issues/786)) ([0d24037](https://github.com/gemini-testing/testplane/commit/0d2403764d5f292826e01a061c019a8b32bb39f7))
* extend AssertViewResultDiff type ([45d1105](https://github.com/gemini-testing/testplane/commit/45d110586092316424db4b1080212fa463382d53))
* extend runnables api on parser events ([85dbc7b](https://github.com/gemini-testing/testplane/commit/85dbc7b2f6b7d686d363bcf7cfe24609596c3e4c))
* fail instead of hang on throws from event handlers ([6c1706a](https://github.com/gemini-testing/testplane/commit/6c1706a9f25471da09ef87c7befd2f62daf53c0d))
* fill tests cache synchronously in workers ([b3b96d3](https://github.com/gemini-testing/testplane/commit/b3b96d3eef34f3da66357fabf1a051f7bcd9d64a))
* find browser in cache according to a browser version ([12df805](https://github.com/gemini-testing/testplane/commit/12df805c21b0933a039925bf166b1438ca64e875))
* fix client code to work on IE11 ([#811](https://github.com/gemini-testing/testplane/issues/811)) ([35159c8](https://github.com/gemini-testing/testplane/commit/35159c8142a3ce925d987e4e226547ed8d647a7a))
* Fix session rejection logic ([6393c6e](https://github.com/gemini-testing/testplane/commit/6393c6ec1d83f9792d06eb0f32a7a90903ed5695))
* fix up opera in webdriverio fork ([5f49845](https://github.com/gemini-testing/testplane/commit/5f4984559bc2b2aef58c520c1a154b24c6e28903))
* Fix url decoration for urls without pathnames ([5df188e](https://github.com/gemini-testing/testplane/commit/5df188e0a05621a15e1744fe57286297b978d892))
* forbid duplicate state names in 'assertView' within one test ([68600ff](https://github.com/gemini-testing/testplane/commit/68600ff8e94eadbe330b54bd61f631c58addedcd))
* free browser in worker test runner ([3d8d4fe](https://github.com/gemini-testing/testplane/commit/3d8d4fe36babb0e9c63eade6c9d8b5ed1d1f1f6f))
* get body width only if it is necessary in "setOrientation" wrapper ([a75655b](https://github.com/gemini-testing/testplane/commit/a75655b10f299d29c2b7540dea3b4ae4601291df))
* grep finds tests by regex and regex-like strings ([acab128](https://github.com/gemini-testing/testplane/commit/acab128ca7283900bd6af82f61344f86b7674f00))
* **halt:** termiante after timeout ends ([c340afc](https://github.com/gemini-testing/testplane/commit/c340afc62056fb9f054e1760d2881c9486eb2dd9))
* handle 'before*' hooks failure correctly ([a0934ba](https://github.com/gemini-testing/testplane/commit/a0934baa28b84a253386b524b9185d7fe61d168e))
* handle cases when error does not have 'hermioneCtx' ([5a82074](https://github.com/gemini-testing/testplane/commit/5a82074bcf3d1b979ee95806b480f46670299a86))
* handle cases when sets from 'CLI' were not been passed ([1054f67](https://github.com/gemini-testing/testplane/commit/1054f673c942656dbf1ab02070789b064a5386e5))
* handle rare cases with unhandled rejections due to circular refs ([fb873ad](https://github.com/gemini-testing/testplane/commit/fb873adc0c3eb9f1fb7cff4572ffae0b3bc37e92))
* handle unhandled rejections ([03676b3](https://github.com/gemini-testing/testplane/commit/03676b32a4d6b8c161c34992b986041c63a05335))
* handle unhandled rejections with circular refs on timeout error ([8c38c66](https://github.com/gemini-testing/testplane/commit/8c38c668f3ecbdaae61f73d740fe916582713aec))
* hermione typings ([8a61ee6](https://github.com/gemini-testing/testplane/commit/8a61ee6a8a7a4fe38d2b1e6d75bfd4687e824fa8))
* hermione.skip skips always for one browser ([8c6de4b](https://github.com/gemini-testing/testplane/commit/8c6de4b7b0e3d0d440961478df7d028c5235d8bb))
* hooks does not have browserId property ([75c7d53](https://github.com/gemini-testing/testplane/commit/75c7d5302b50eb050b806636e5296719a80a75de))
* **ie11:** execute script correctly on scroll page ([6481824](https://github.com/gemini-testing/testplane/commit/64818242bf1d12e619f51d716b2b2ba9913cd2f8))
* ignore "execution context was destroyed" error from puppeteer ([d3ee42f](https://github.com/gemini-testing/testplane/commit/d3ee42fe12d1b97a037d44209d6601490892c5ac))
* ignore failed tests from mocha ([bd41074](https://github.com/gemini-testing/testplane/commit/bd41074cd352ac832eb4880251c70f266b2b733b))
* ignore memory leaks warnings for mocha suites ([93ed298](https://github.com/gemini-testing/testplane/commit/93ed29813ec6e6596b97024310ac781902eafcce))
* ignore objectId puppeteer error ([#832](https://github.com/gemini-testing/testplane/issues/832)) ([f7fa626](https://github.com/gemini-testing/testplane/commit/f7fa6265238388a83fd562e7f3ce49475e79e2dc))
* ignore ProtocolError unhandled rejections ([bf80946](https://github.com/gemini-testing/testplane/commit/bf8094658e2469b3e5cf9313b584c9d1e4d324b3))
* ignore puppeteer ProtocolError in workers ([d46f8f6](https://github.com/gemini-testing/testplane/commit/d46f8f6bb3100c5cafba878c28675b2465800697))
* ignore TargetCloseError ([305c6c1](https://github.com/gemini-testing/testplane/commit/305c6c1610312e025b02f49bf0692e446739fa1f))
* improve the algorithm of retries ([b2d91b7](https://github.com/gemini-testing/testplane/commit/b2d91b7bb2e675b5c723cb6487b3efb9dcf3dcf1))
* incorrect work of "grep" option ([0c355fe](https://github.com/gemini-testing/testplane/commit/0c355febfb377e9e2a11bee2e1d9c3249f897f1c))
* increment stats for each test result ([cdb1ac3](https://github.com/gemini-testing/testplane/commit/cdb1ac3f80aadabe6c4a65c55a06b5f56be602cc))
* init save diff function in master process ([c263d87](https://github.com/gemini-testing/testplane/commit/c263d8736fd5c63755a69bb4ecac0ad6044f2aaa))
* init temp in master process ([5dd0dee](https://github.com/gemini-testing/testplane/commit/5dd0dee60357bd2ff03e33c1ff7fbeca4ef5cd65))
* load plugins early ([5c00a24](https://github.com/gemini-testing/testplane/commit/5c00a24d8bc9c53b95028773b34f4a24f966aa73))
* log an error while trying to register ts-node ([e5f4323](https://github.com/gemini-testing/testplane/commit/e5f4323ec8cae3f415dd12ad54e35909b482e082))
* logging for unhandledRejection ([e8bb9f3](https://github.com/gemini-testing/testplane/commit/e8bb9f38998df38b80128665f65e573be362d941))
* logic of ignore caret option on ImageDiffError ([d44c92a](https://github.com/gemini-testing/testplane/commit/d44c92a8e19f1d287af07228e9dafab31fe8d1e4))
* Make sync and async events pass through separately ([87722ba](https://github.com/gemini-testing/testplane/commit/87722bac60f500513225e50ea417bb70d28bd2cc))
* make test.id looks like a property ([9964432](https://github.com/gemini-testing/testplane/commit/9964432d9443b271ef446bb9c3ea05608052d083))
* mark session as broken on cursor reset error ([9083e8d](https://github.com/gemini-testing/testplane/commit/9083e8de90dc5111bbfc5ea51a92821943f5e1ad))
* meta randomly does not contain 'pid' ([1e476c9](https://github.com/gemini-testing/testplane/commit/1e476c99f577e8ec4cb6a2433aa94d29d13eff35))
* migrate png-img -> sharp ([35e9429](https://github.com/gemini-testing/testplane/commit/35e942918308279b4d6f552092d99e151eac271d))
* **mocha-adapter:** restore browser at each mocha reinitialization ([44bc801](https://github.com/gemini-testing/testplane/commit/44bc801d0ee5465870f066c4b838743401574dac))
* more proper lists ([afca4f4](https://github.com/gemini-testing/testplane/commit/afca4f42c55e067eb2735da70a93a8ba80db1097))
* move calibrate script to client-script dir ([b3ae6a3](https://github.com/gemini-testing/testplane/commit/b3ae6a3b8593f65f941c683cd7d716e518d3790e))
* move client scripts out of scripts directory ([1b4f6b6](https://github.com/gemini-testing/testplane/commit/1b4f6b6a653ddd8ebdbd2e1146033c62da907439))
* move cursor relative to the center of body when using "resetCursor" option ([36c4f36](https://github.com/gemini-testing/testplane/commit/36c4f367cf2e2a360dda5f7bb9bbceecdb188fcf))
* move mocha and wdio types from dev deps to deps ([c23a0b9](https://github.com/gemini-testing/testplane/commit/c23a0b96139f3d52992c8189cf967a6639b2ef01))
* never use browser session again if it fails on initializition ([1036969](https://github.com/gemini-testing/testplane/commit/10369692a27b9b253660731655d73c8fd2790de8))
* optional timeouts by default does not equal to httpTimeout ([aa670d9](https://github.com/gemini-testing/testplane/commit/aa670d9029b8758965492d423ced4076b302acff))
* pass extra field on file events to fix breaking change ([10c0a7f](https://github.com/gemini-testing/testplane/commit/10c0a7ffb7a6c8081a300d5900b3cf6ec1ee4f13))
* pass meta info from workers to the main process ([0e8580a](https://github.com/gemini-testing/testplane/commit/0e8580a2833c429442c9d1e256c0661b1a6dc313))
* passthrough "pixelRatio" to image comparator ([6775838](https://github.com/gemini-testing/testplane/commit/677583875595800306fc6d9dc5c7eac10015ad0e))
* prepareScreenshot method should throw error from browser ([10164db](https://github.com/gemini-testing/testplane/commit/10164db34f44dacdfc43901e29b1b64ee7f636fc))
* proper headers in readme ([ac49782](https://github.com/gemini-testing/testplane/commit/ac49782b1a6b050376b9446cdb686d45177abc6b))
* proxy events before workers init ([#417](https://github.com/gemini-testing/testplane/issues/417)) ([8b2456a](https://github.com/gemini-testing/testplane/commit/8b2456aa7385c27fe592babbb81ed3a9eba0c31a))
* **proxy-reporter:** rewrite on ES6 ([69ffefe](https://github.com/gemini-testing/testplane/commit/69ffefe38336ba008ee7402767cc2905301630cd))
* reinit browser in worker with his session options ([585f5fa](https://github.com/gemini-testing/testplane/commit/585f5faeab68f292af51236ed67c009aa0d6a695))
* remove child nodes when parent leaves callstack ([8fade7b](https://github.com/gemini-testing/testplane/commit/8fade7b2f43aef23e6cec5b6568e80d48da3d05c))
* remove deprecated options ([cf1d69f](https://github.com/gemini-testing/testplane/commit/cf1d69fab8fe018b051239a7357a90e014d3383f))
* remove features related to wdio native history ([8205bf3](https://github.com/gemini-testing/testplane/commit/8205bf38a6de59f772a56af8287b7951d3943298))
* remove unused "teamcity" reporter ([56a9293](https://github.com/gemini-testing/testplane/commit/56a9293a49009e89eb20061fc28ba72977868bd4))
* removed temp hack with error catching on set page load timeout ([073cac7](https://github.com/gemini-testing/testplane/commit/073cac7c9e8e0addbb09f6c086dc759c9b9b8ecd))
* Replace mocha timeouts with promise timeouts ([9d648d9](https://github.com/gemini-testing/testplane/commit/9d648d9e4cce3970605c78b875d41ec79f5da39d))
* reset cursor correctly for body with negative coords ([a0b8cd6](https://github.com/gemini-testing/testplane/commit/a0b8cd64d6cece993b801e2ea5b9c82b59163873))
* reset window size on default before the test is started ([8357206](https://github.com/gemini-testing/testplane/commit/8357206b8391675325fe3adcbfbcc017e1db7324))
* resolve file field correctly for exports mocha interface ([#949](https://github.com/gemini-testing/testplane/issues/949)) ([99a7ed1](https://github.com/gemini-testing/testplane/commit/99a7ed10460eba412896a5af0ed9d39e52a7231a))
* return origCommand type to overwriteCommand ([f2039a0](https://github.com/gemini-testing/testplane/commit/f2039a02b743622ab709b7a43977990c1992add5))
* reuse session caps in worker from master ([5c70fe0](https://github.com/gemini-testing/testplane/commit/5c70fe074e9f58125f5cdc50d49c0cb9066fc88a))
* round xOffset and yOffset when resetting cursor ([#837](https://github.com/gemini-testing/testplane/issues/837)) ([79786cd](https://github.com/gemini-testing/testplane/commit/79786cd030a845e26d0bbe677a7bb90e5887456f))
* running of tests with option 'grep' fails with exception ([4c80583](https://github.com/gemini-testing/testplane/commit/4c805837298e0d5e6b08dc0c8ab0607c07f7322a))
* **screenshot:** handle viewport overflow properly ([2142cd8](https://github.com/gemini-testing/testplane/commit/2142cd8ff4ef5cb65dc87af5e0a144225bd8137a))
* scrollBy using scrollTo ([95d7b06](https://github.com/gemini-testing/testplane/commit/95d7b06cc3e111fd79589357b226f0fee82acb19))
* set default port "4444" if it is not specified in "gridUrl" ([5dae3c7](https://github.com/gemini-testing/testplane/commit/5dae3c77ec36c550771d664a5406562138e9ec12))
* set default port "4444" if it is not specified in "gridUrl" ([5de53aa](https://github.com/gemini-testing/testplane/commit/5de53aaae2cf0a6802bfac99337b1fc430d7047b))
* set id method even for skipped suites by mocha ([ce7bc89](https://github.com/gemini-testing/testplane/commit/ce7bc89cee95991d37eb3cf81311b2549193d095))
* set meta info on before each hook ([f0ea113](https://github.com/gemini-testing/testplane/commit/f0ea11379b27360d9f5d7428388efe0126a91947))
* set orientation before each test ([5dee565](https://github.com/gemini-testing/testplane/commit/5dee565e60f8343c98a536a2e06ddd9ca4ede02d))
* set screenshotMode to viewport on android browsers ([326f5a7](https://github.com/gemini-testing/testplane/commit/326f5a7da69fa1dd7258948adc1c296fed383e68))
* set timeout for execution screenshot on reject ([dd73f3e](https://github.com/gemini-testing/testplane/commit/dd73f3e6753c24299034a2c0843310894e010afe))
* show error with stack trace on call hermione.halt method ([61cfc26](https://github.com/gemini-testing/testplane/commit/61cfc269ae356c342967126faed5bd31017ccdf8))
* specify the realease branch of forked 'worker-farm' ([649cec6](https://github.com/gemini-testing/testplane/commit/649cec6a70c39adfe39ead3035d5d0057c02eeb8))
* **stats:** correctly handle events happened after first getResult call ([7b9088c](https://github.com/gemini-testing/testplane/commit/7b9088c8cc0d4cefea9c17067a635005d744cb2e))
* stop emitting suite end after each test ([e78eed7](https://github.com/gemini-testing/testplane/commit/e78eed7e2812447a64e62891eba944e3706ca15b))
* stop escaping of special symbols in grep ([9bbb028](https://github.com/gemini-testing/testplane/commit/9bbb028c5b2f52060bb232d48726efb7908c5c1c))
* stringify safely object arguments in command history ([eb87464](https://github.com/gemini-testing/testplane/commit/eb87464b088353d13278d8abf7a58cf085214284))
* suite.id() no longer depends on parsing order ([d13d82d](https://github.com/gemini-testing/testplane/commit/d13d82d77fad374ffee7edda92ee88cea75cd423))
* sync config in worker before running tests ([ba68fea](https://github.com/gemini-testing/testplane/commit/ba68feab3b19834c124e7e8eb8b037011c8ca128))
* system.debug config field ([4f3e01c](https://github.com/gemini-testing/testplane/commit/4f3e01cf5c61021e13b7f70b2041fe938dfe6929))
* take into account zero height of ignore element ([d8a3afd](https://github.com/gemini-testing/testplane/commit/d8a3afdef6a5885929b5655b5caa0e70d166dcd7))
* temporary overwrite "scrollIntoView" command with bug ([2fb4474](https://github.com/gemini-testing/testplane/commit/2fb4474bd169c85f555569b79d0a33fd674d7141))
* test frees random browser ([f1419e6](https://github.com/gemini-testing/testplane/commit/f1419e6de6f57995b617553380b4a3ee3ef5cadf))
* test meta from worker totally redefines test meta from master ([df2b97e](https://github.com/gemini-testing/testplane/commit/df2b97e106ff7801c2e1edf6201025c3335be350))
* **test-collection:** compare test titles with trim ([e245993](https://github.com/gemini-testing/testplane/commit/e2459931449397a5306862d1654e8ba8ebb998f9))
* **test-runner:** out of bound error on cursor reset ([687b669](https://github.com/gemini-testing/testplane/commit/687b6691a19a23d83b69501c1cc81541f25646d3))
* test.hermioneCtx not acceptable inside test callback ([c069f57](https://github.com/gemini-testing/testplane/commit/c069f5736f9e8cced5238a06617c4e39efdd65f0))
* TestCollection: do not add empty browser to properties ([63bdc77](https://github.com/gemini-testing/testplane/commit/63bdc77b7f639e736fec19433dbbf785857c8939))
* tests do not fail on assert view fails ([1a5ed83](https://github.com/gemini-testing/testplane/commit/1a5ed83e812d818b3a852acc6d47d412678783a2))
* tests doesn't run ([1484bb9](https://github.com/gemini-testing/testplane/commit/1484bb905e760363085ed4ee1182acc109991223))
* the output to file path on 'before all' hook ([1378e75](https://github.com/gemini-testing/testplane/commit/1378e7551ab32854a42327d10c8fe54d9187d08c))
* throw error on invalid reference ([7b74f1b](https://github.com/gemini-testing/testplane/commit/7b74f1b04cf7977d3eabdb930717de08533d5fe9))
* throw error when there are no tests found ([ec9eed1](https://github.com/gemini-testing/testplane/commit/ec9eed1c5f08057cb9d0c9179d341acbe6b04a3c))
* throw error when there is no "body" when resetting cursor pos ([b7e8925](https://github.com/gemini-testing/testplane/commit/b7e8925daa59b9136ad75c1912e4c0e857b48eb1))
* type-safe overwriteCommand ([#885](https://github.com/gemini-testing/testplane/issues/885)) ([b10d17b](https://github.com/gemini-testing/testplane/commit/b10d17ba1ac0ca68354e990b4e2049d28b6da8e4))
* types for describe, it ([9e0d2b9](https://github.com/gemini-testing/testplane/commit/9e0d2b9637768d0283ddca1742e5cc86a303179e))
* **types:** add 'headers' property to config ([a0061d2](https://github.com/gemini-testing/testplane/commit/a0061d2276c17d190c6f670bd45ac518e3f78621))
* **types:** set correct type for "sets" field in config ([0164875](https://github.com/gemini-testing/testplane/commit/0164875e02604f3f555df927e68a0ba19193ab49))
* typings ([e40018b](https://github.com/gemini-testing/testplane/commit/e40018bf0fa2dee38f0ca08cc5b69c9a84a32331))
* typings for browser interface ([e0f89b8](https://github.com/gemini-testing/testplane/commit/e0f89b844e0261df31123a6a55c14b4cfb9b61ad))
* up gemini-core version ([c7dda90](https://github.com/gemini-testing/testplane/commit/c7dda908ddf0258f2dc033ec7f53d504ca00d7ab))
* up version gemini-core to support Node 16 ([6b5af5d](https://github.com/gemini-testing/testplane/commit/6b5af5ddf4af6dae1b33854d19c53a1432966eb2))
* update gemini-core to 3.6.1 ([8e5ac84](https://github.com/gemini-testing/testplane/commit/8e5ac8413ca257ed7e3d977c06302b80086edc19))
* update gemini-core to 6.3.6 ([452bc69](https://github.com/gemini-testing/testplane/commit/452bc6956007fbcd75cd3cd5b8e7108a9fc4a4c9))
* update gemini-core to version with png-img with prebuilt binaries ([219e900](https://github.com/gemini-testing/testplane/commit/219e900227bd1a7dacb169c9a2afd8f6b55d4be9))
* update package-lock.json ([7e7dee0](https://github.com/gemini-testing/testplane/commit/7e7dee0636431e081b57d70c49c8c2f296384a94))
* update png-img to 5.0.1 with windows build fix ([f3a00d1](https://github.com/gemini-testing/testplane/commit/f3a00d189c60cab571473c95cfd02bd3157c2c5a))
* update runtime config before creating runner ([fc22e05](https://github.com/gemini-testing/testplane/commit/fc22e054311f7a1e132514c7dd187d39188f88c2))
* update webdriver.io fork with keep-alive fix ([8926d5d](https://github.com/gemini-testing/testplane/commit/8926d5dc8d3ef6cb673a7d412bc752d5eb836cf6))
* update webdriverio fork to 4.9.11 ([2f0b1fc](https://github.com/gemini-testing/testplane/commit/2f0b1fca3f9e96ac6de94884b721e0503fd42125))
* use 'any' instead of 'unknown' typing for ctx ([637b2f5](https://github.com/gemini-testing/testplane/commit/637b2f50aca3680ac64f8f2ef93e2ae7c00f64e5))
* use "-r" option for require module and not for "--reporter" ([ca35198](https://github.com/gemini-testing/testplane/commit/ca35198a4dfaf159ebbb12e332704aa8df184886))
* use exact version of webdriverio@8.13.4 ([f7ea267](https://github.com/gemini-testing/testplane/commit/f7ea267decebc00397276d999694532bb2aabfa4))
* use gemini-core with stable looks-same ([0173a7a](https://github.com/gemini-testing/testplane/commit/0173a7ad114fafed77b02eaf213c97bce18b74b4))
* use new typings from webdriverio ([63d1a5a](https://github.com/gemini-testing/testplane/commit/63d1a5a160cf43c603a2340832db7aac992e7886))
* use nodenext moduleResolution with ts-node ([#918](https://github.com/gemini-testing/testplane/issues/918)) ([34a8ea8](https://github.com/gemini-testing/testplane/commit/34a8ea8c4da89db666d87092335a48fcde5519cf))
* use sessionId in the name of free browser event ([782305e](https://github.com/gemini-testing/testplane/commit/782305e1d0aa30b17b23d707a7aab92f5cf4f1df))
* use strict version of webdriverio ([a111f9b](https://github.com/gemini-testing/testplane/commit/a111f9b8f853660eda4aa631b7f8e0c0e4c21e6d))
* use suite position in file instead of global position to generate id ([fd3716a](https://github.com/gemini-testing/testplane/commit/fd3716a3c03aab3a2362da6a9ba997a90aec9c1d))
* use test.clone instead of Object.create(test) to avoid test modification ([23dbee7](https://github.com/gemini-testing/testplane/commit/23dbee7800c5081271fb19611399b053cd974300))
* use undefined as a default value for browserVersion and browserId properties ([ddfe85f](https://github.com/gemini-testing/testplane/commit/ddfe85f0c600370f1d7f6b0ed04616a656e33fbc))
* use WebdriverIO.Browser instead of webdriverio browser ([fcd6c50](https://github.com/gemini-testing/testplane/commit/fcd6c5098e739ec99426041198240bc13d7b8c6e))
* vulnerabilities ([7c3e942](https://github.com/gemini-testing/testplane/commit/7c3e942292d3eab9f84a420246343134f2eabf94))
* **worker/test-runner:** take the error screenshot on every test fail ([2199e0b](https://github.com/gemini-testing/testplane/commit/2199e0b57ece8e0f46d0f7be141c44827f417d27))
* **worker:** load external modules from "--require" option ([1abb66a](https://github.com/gemini-testing/testplane/commit/1abb66ae4056b3bb2e6b90c03555e04a0996a2e4))

## [8.13.0](https://github.com/gemini-testing/testplane/compare/v8.12.2...v8.13.0) (2024-06-19)


### Features

* add relativePath to refImg ([0bb23cf](https://github.com/gemini-testing/testplane/commit/0bb23cf7b05b16bc3cdcdd176be888c2fb161b04))

### [8.12.2](https://github.com/gemini-testing/testplane/compare/v8.12.1...v8.12.2) (2024-06-18)


### Bug Fixes

* pass extra field on file events to fix breaking change ([10c0a7f](https://github.com/gemini-testing/testplane/commit/10c0a7ffb7a6c8081a300d5900b3cf6ec1ee4f13))

### [8.12.1](https://github.com/gemini-testing/testplane/compare/v8.12.0...v8.12.1) (2024-06-14)


### Bug Fixes

* resolve file field correctly for exports mocha interface ([#949](https://github.com/gemini-testing/testplane/issues/949)) ([99a7ed1](https://github.com/gemini-testing/testplane/commit/99a7ed10460eba412896a5af0ed9d39e52a7231a))

## [8.12.0](https://github.com/gemini-testing/testplane/compare/v8.11.7...v8.12.0) (2024-06-09)


### Features

* **ct:** support hot module replacement ([71628ce](https://github.com/gemini-testing/testplane/commit/71628ce39d7e96978c9fcbf9059f05113bf1c352))


### Bug Fixes

* **ct:** do not fail on log html elements ([016dc45](https://github.com/gemini-testing/testplane/commit/016dc45ec6cb083c0c8db75192636c1795563c51))
* **ct:** use correct type for config from vite ([b152038](https://github.com/gemini-testing/testplane/commit/b15203876b8a0ca8cc323a7c242955008cb94c87))

### [8.11.7](https://github.com/gemini-testing/testplane/compare/v8.11.6...v8.11.7) (2024-06-05)


### Bug Fixes

* build client scripts bundle on build time ([b3ae6a3](https://github.com/gemini-testing/testplane/commit/b3ae6a3b8593f65f941c683cd7d716e518d3790e))

### [8.11.6](https://github.com/gemini-testing/testplane/compare/v8.11.5...v8.11.6) (2024-05-29)


### Bug Fixes

* types for describe, it ([9e0d2b9](https://github.com/gemini-testing/testplane/commit/9e0d2b9637768d0283ddca1742e5cc86a303179e))

### [8.11.5](https://github.com/gemini-testing/testplane/compare/v8.11.4...v8.11.5) (2024-05-29)


### Bug Fixes

* "assertView", "moveCursorTo", "executionContext" and "currentTest" types ([bd4e898](https://github.com/gemini-testing/testplane/commit/bd4e8980fcffbad59af6df48726418586b1bae4a))
* **ct:** correctly support custom element commands ([5817e92](https://github.com/gemini-testing/testplane/commit/5817e92916be7e97940cec1940bc19296be28687))

### [8.11.4](https://github.com/gemini-testing/testplane/compare/v8.11.3...v8.11.4) (2024-05-16)


### Bug Fixes

* ignore "execution context was destroyed" error from puppeteer ([d3ee42f](https://github.com/gemini-testing/testplane/commit/d3ee42fe12d1b97a037d44209d6601490892c5ac))

### [8.11.3](https://github.com/gemini-testing/testplane/compare/v8.11.2...v8.11.3) (2024-05-16)


### Bug Fixes

* correctly screen element after moveTo ([b65169e](https://github.com/gemini-testing/testplane/commit/b65169e3219b54afa382fbe69e5dfbf02916c3cb))

### [8.11.2](https://github.com/gemini-testing/testplane/compare/v8.11.1...v8.11.2) (2024-05-15)


### Bug Fixes

* correctly require plugins with yarn+pnp ([7708cf8](https://github.com/gemini-testing/testplane/commit/7708cf8edd5c3bacc3e27146149302afd86c7746))
* correctly specify "testplaneCtx.assertViewResults" type ([e10c718](https://github.com/gemini-testing/testplane/commit/e10c7184bbd326ca550224c7246ba3d6b3acf333))

### [8.11.1](https://github.com/gemini-testing/testplane/compare/v8.11.0...v8.11.1) (2024-05-06)


### Bug Fixes

* dont remove imports in nodejs env ([f132eeb](https://github.com/gemini-testing/testplane/commit/f132eebc12d0dcd71e5897503fd5d1a1ad526c50))

## [8.11.0](https://github.com/gemini-testing/testplane/compare/v8.10.1...v8.11.0) (2024-05-01)


### Features

* add error snippets ([a78ba06](https://github.com/gemini-testing/testplane/commit/a78ba064dd98ce0335d5e6f7d6ac2b0746ca4ac3))
* enhance stacktraces ([36bb693](https://github.com/gemini-testing/testplane/commit/36bb693e3df7485ad1b1016d3c2f1f88560da29b))

### [8.10.1](https://github.com/gemini-testing/testplane/compare/v8.10.0...v8.10.1) (2024-04-24)


### Bug Fixes

* use nodenext moduleResolution with ts-node ([#918](https://github.com/gemini-testing/testplane/issues/918)) ([34a8ea8](https://github.com/gemini-testing/testplane/commit/34a8ea8c4da89db666d87092335a48fcde5519cf))

## [8.10.0](https://github.com/gemini-testing/testplane/compare/v0.1.3...v8.10.0) (2024-04-23)


### Bug Fixes

* **ct:** generate url in format "/run-uuids/:uuid" ([dd61276](https://github.com/gemini-testing/testplane/commit/dd612765119baa97b777fad577d1b5d105e6ffff))
* **ct:** read tsx files with types ([c8fcd87](https://github.com/gemini-testing/testplane/commit/c8fcd87f45f9b4aa6b17bc51331d981f2f1e0d91))

### [0.1.3](https://github.com/gemini-testing/testplane/compare/v0.1.2...v0.1.3) (2024-04-21)


### Features

* add ability to use dev server ([daf1bb6](https://github.com/gemini-testing/testplane/commit/daf1bb6443c327d10514c7e67c75501b8beedfc4))


### Bug Fixes

* correctly connect to vite server from clients (worker, browser) ([d77ee9d](https://github.com/gemini-testing/testplane/commit/d77ee9dbcf02ccb4c8be211afcb18dc7e4ce4ea2))
* correctly read tsx files with types ([ac77d36](https://github.com/gemini-testing/testplane/commit/ac77d36cd44eca491b39d727a39d8159c73ac34a))

### [0.1.2](https://github.com/gemini-testing/testplane/compare/v0.1.1...v0.1.2) (2024-04-16)


### Features

* ability to read tests in ".jsx" and ".tsx" files ([2884a7e](https://github.com/gemini-testing/testplane/commit/2884a7ef44f19575421cbd5d50c0533cd93d75e6))
* ability to run unit tests in browser ([0e9f9ac](https://github.com/gemini-testing/testplane/commit/0e9f9accae4a0998a03dfa74377b748976620440))
* add ability to show user log in component tests ([772cf09](https://github.com/gemini-testing/testplane/commit/772cf09b3609e3d9c3883dfe69cc4ae7649d5616))
* add ability to use browser in component tests ([022e051](https://github.com/gemini-testing/testplane/commit/022e0516f7a9a21a87fb51f773bcf10a37990f6d))
* add ability to use expect in component tests ([f3f97a7](https://github.com/gemini-testing/testplane/commit/f3f97a741622863062b5497a95595f933229c522))


### Bug Fixes

* correctly mock "debug", "saveScreenshot" and "savePDF" ([202af7d](https://github.com/gemini-testing/testplane/commit/202af7d82f2d9741aa5b0478bc14c793974eb059))

### [0.1.1](https://github.com/gemini-testing/testplane/compare/v0.1.0...v0.1.1) (2024-04-14)

### [8.8.1](https://github.com/gemini-testing/hermione/compare/v8.8.0...v8.8.1) (2024-04-05)


### Bug Fixes

* do not remove spaces in runnable title ([df139ea](https://github.com/gemini-testing/hermione/commit/df139eac20ce00d4960b46c0b6ea57e7da06baf8))

## [8.8.0](https://github.com/gemini-testing/hermione/compare/v8.7.2...v8.8.0) (2024-04-03)


### Features

* add ability to extend "hermione" global variable ([f4c0cec](https://github.com/gemini-testing/hermione/commit/f4c0cec57c107e17fae39918542df9c039216f5e))

### [8.7.2](https://github.com/gemini-testing/hermione/compare/v8.7.1...v8.7.2) (2024-03-29)


### Bug Fixes

* export HermioneCtx type ([363ed89](https://github.com/gemini-testing/hermione/commit/363ed89944411c516bef42dd3f75a1863e5dc0da))

### [8.7.1](https://github.com/gemini-testing/hermione/compare/v8.7.0...v8.7.1) (2024-03-28)


### Bug Fixes

* return origCommand type to overwriteCommand ([f2039a0](https://github.com/gemini-testing/hermione/commit/f2039a02b743622ab709b7a43977990c1992add5))

## [8.7.0](https://github.com/gemini-testing/hermione/compare/v8.6.0...v8.7.0) (2024-03-27)


### Features

* add ability to extend hermione.ctx typings ([540893c](https://github.com/gemini-testing/hermione/commit/540893cd3cdadcdd25cfc4d2a0b6a114a77cc164))

## [8.6.0](https://github.com/gemini-testing/hermione/compare/v8.5.2...v8.6.0) (2024-03-26)


### Features

* export Key from webdriverio ([57e345e](https://github.com/gemini-testing/hermione/commit/57e345e006ab8318bd733ec0ea6c99a17baade4e))

### [8.5.2](https://github.com/gemini-testing/hermione/compare/v8.5.1...v8.5.2) (2024-03-26)


### Bug Fixes

* type-safe overwriteCommand ([#885](https://github.com/gemini-testing/hermione/issues/885)) ([b10d17b](https://github.com/gemini-testing/hermione/commit/b10d17ba1ac0ca68354e990b4e2049d28b6da8e4))

### [8.5.1](https://github.com/gemini-testing/hermione/compare/v8.5.0...v8.5.1) (2024-03-20)


### Bug Fixes

* add missing command types (moveCursorTo and openAndWait) ([#876](https://github.com/gemini-testing/hermione/issues/876)) ([5268a44](https://github.com/gemini-testing/hermione/commit/5268a4435a42e42b2aad4b245e8ae93a136f676f))

## [8.5.0](https://github.com/gemini-testing/hermione/compare/v8.4.1...v8.5.0) (2024-03-18)


### Features

* add ability to enable new Chrome headless mode ([cbc4860](https://github.com/gemini-testing/hermione/commit/cbc486079f0989bdaf75eab9802f2b60593142d2))

### [8.4.1](https://github.com/gemini-testing/hermione/compare/v8.4.0...v8.4.1) (2024-03-14)


### Bug Fixes

* ignore TargetCloseError ([305c6c1](https://github.com/gemini-testing/hermione/commit/305c6c1610312e025b02f49bf0692e446739fa1f))

## [8.4.0](https://github.com/gemini-testing/hermione/compare/v8.3.0...v8.4.0) (2024-03-13)


### Features

* add ability to use plugin's default export ([f1799b0](https://github.com/gemini-testing/hermione/commit/f1799b0246feae24d34c21fae226e96c534d6be5))

## [8.3.0](https://github.com/gemini-testing/hermione/compare/v8.2.2...v8.3.0) (2024-03-12)


### Features

* add ability to use default export in .hermione.conf file ([b4e1d6c](https://github.com/gemini-testing/hermione/commit/b4e1d6c9748c0d67381b5ac5e043a59675aaff56))
* add ability to use import and export in test files ([8bb43e7](https://github.com/gemini-testing/hermione/commit/8bb43e70a892368653189db5a53b169840838db2))


### Bug Fixes

* add ability to specify runStep resolved value ([e7f1130](https://github.com/gemini-testing/hermione/commit/e7f113071f26b40d3f82514fbeb77c06fdca4598))
* add getConfig command typings ([5889066](https://github.com/gemini-testing/hermione/commit/5889066aab9634f402eeb971bb908fcc5e919a08))
* add typings for overwriteCommand: custom commands ([420ec8b](https://github.com/gemini-testing/hermione/commit/420ec8bb3d86a2eac8ebb0aea6b02e592a92365b))
* export AssertViewOpts type ([2b1a4dd](https://github.com/gemini-testing/hermione/commit/2b1a4ddb9dbdc17e9077d3561ce1718403eded7e))
* use WebdriverIO.Browser instead of webdriverio browser ([fcd6c50](https://github.com/gemini-testing/hermione/commit/fcd6c5098e739ec99426041198240bc13d7b8c6e))

### [8.2.2](https://github.com/gemini-testing/hermione/compare/v8.2.1...v8.2.2) (2024-03-07)


### Bug Fixes

* correctly screen elements inside iframes ([9ecf164](https://github.com/gemini-testing/hermione/commit/9ecf164f972b067084c1fa3d4b0d58c0dd3ee91f))

## [8.2.1](https://github.com/gemini-testing/hermione/compare/v8.2.0...v8.2.1) (2024-03-04)


### Bug Fixes

* extend AssertViewResultDiff type ([45d1105](https://github.com/gemini-testing/hermione/commit/45d110586092316424db4b1080212fa463382d53))

## [8.2.0](https://github.com/gemini-testing/hermione/compare/v8.0.5...v8.2.0) (2024-02-29)


### Features

* add ability to specify ignoreDiffPixelCount in assertView ([32242e1](https://github.com/gemini-testing/hermione/commit/32242e15d3ed84ac52a126ca93e5a1cb4a97c34c))
* export TestError type ([#848](https://github.com/gemini-testing/hermione/issues/848)) ([f860b7c](https://github.com/gemini-testing/hermione/commit/f860b7c3a93e7c1cbac8347d63d27d64c00817ea))

## [8.1.0](https://github.com/gemini-testing/hermione/compare/v8.0.6...v8.1.0) (2024-02-20)


### Features

* add new command `moveCursorTo` which move cursro from left-top corener of the element


### Bug Fixes

* move cursor relative to the center of body when using "resetCursor" option ([36c4f36](https://github.com/gemini-testing/hermione/commit/36c4f367cf2e2a360dda5f7bb9bbceecdb188fcf))

### [8.0.6](https://github.com/gemini-testing/hermione/compare/v8.0.5...v8.0.6) (2024-02-12)


### Bug Fixes

* do not lost "testXReqId" when using "parallelLimit" ([8d6d82a](https://github.com/gemini-testing/hermione/commit/8d6d82a3ff810c8be437a014f40fee7b70cddd9f))

### [8.0.5](https://github.com/gemini-testing/hermione/compare/v8.0.4...v8.0.5) (2024-01-31)


### Bug Fixes

* round xOffset and yOffset when resetting cursor ([#837](https://github.com/gemini-testing/hermione/issues/837)) ([79786cd](https://github.com/gemini-testing/hermione/commit/79786cd030a845e26d0bbe677a7bb90e5887456f))

### [8.0.4](https://github.com/gemini-testing/hermione/compare/v8.0.3...v8.0.4) (2024-01-25)


### Bug Fixes

* typings ([e40018b](https://github.com/gemini-testing/hermione/commit/e40018bf0fa2dee38f0ca08cc5b69c9a84a32331))

### [8.0.3](https://github.com/gemini-testing/hermione/compare/v8.0.2...v8.0.3) (2024-01-24)


### Bug Fixes

* correctly disable test execution timeout in repl mode ([bc91823](https://github.com/gemini-testing/hermione/commit/bc918235fb259b31d21c33cce23eae5b07119778))

### [8.0.2](https://github.com/gemini-testing/hermione/compare/v8.0.1...v8.0.2) (2024-01-24)


### Bug Fixes

* do not require .d.ts file ([#831](https://github.com/gemini-testing/hermione/issues/831)) ([91708d2](https://github.com/gemini-testing/hermione/commit/91708d2eec83c790591494706d607e1dcc8c4b77))
* ignore objectId puppeteer error ([#832](https://github.com/gemini-testing/hermione/issues/832)) ([f7fa626](https://github.com/gemini-testing/hermione/commit/f7fa6265238388a83fd562e7f3ce49475e79e2dc))

### [8.0.1](https://github.com/gemini-testing/hermione/compare/v8.0.0...v8.0.1) (2024-01-23)


### Bug Fixes

* add typings for "switchToRepl" and "clearSession" commands ([0e85f3b](https://github.com/gemini-testing/hermione/commit/0e85f3ba6efb00778ecccde9a17260c65a7e842a))

## [8.0.0](https://github.com/gemini-testing/hermione/compare/v8.0.0-beta.3...v8.0.0) (2024-01-17)


### Features

* add "clearSession" browser command ([7114cd5](https://github.com/gemini-testing/hermione/commit/7114cd57bcec93a9a0b4d35ae300151ef5865a07))
* add ability to use devtools procotol through cli option ([852f375](https://github.com/gemini-testing/hermione/commit/852f375f899a26cfa7e57b1bfded87a0aa8284ff))
* add basic unhandled rejection stack trace ([5b1db43](https://github.com/gemini-testing/hermione/commit/5b1db438e7bb51b375aad13f6d3c6aedcd2feca3))
* generate "X-Request-ID" header for each browser request ([d40cd6a](https://github.com/gemini-testing/hermione/commit/d40cd6a9e9bf9182ab1552c52e0199cf8e1d00c5))
* implement REPL interface to debug tests ([8c17648](https://github.com/gemini-testing/hermione/commit/8c1764810da85258ff86dcac0d12f35b6eb7e1dc))


### Bug Fixes

* ability to disable tests isolation ([51b87fd](https://github.com/gemini-testing/hermione/commit/51b87fd21ddfefe0ee46bb1105ee61ccc14d5d92))
* correctly disable animations in inframes for ios ([5db5fa8](https://github.com/gemini-testing/hermione/commit/5db5fa87bec3e645204bca6bc7fbe580e0954ba6))
* correctly generate test x request id for each test in one browser ([443056b](https://github.com/gemini-testing/hermione/commit/443056bb7f4b29b2694516d041e4c0403b9669e3))
* correctly switch between iframes on disable animation ([eabea08](https://github.com/gemini-testing/hermione/commit/eabea08feaa7bbb1b1f4e74a7a473115be72444a))
* fix client code to work on IE11 ([#811](https://github.com/gemini-testing/hermione/issues/811)) ([35159c8](https://github.com/gemini-testing/hermione/commit/35159c8142a3ce925d987e4e226547ed8d647a7a))
* ignore puppeteer ProtocolError in workers ([d46f8f6](https://github.com/gemini-testing/hermione/commit/d46f8f6bb3100c5cafba878c28675b2465800697))

## [8.0.0-beta.3](https://github.com/gemini-testing/hermione/compare/v8.0.0-beta.1...v8.0.0-beta.3) (2023-11-14)


### Features

* export TestCollection and Test types ([#806](https://github.com/gemini-testing/hermione/issues/806)) ([a4771a2](https://github.com/gemini-testing/hermione/commit/a4771a24fc0f10ef647b989461096b5cfe4d50ad))

## [8.0.0-beta.2](https://github.com/gemini-testing/hermione/compare/v8.0.0-beta.1...v8.0.0-beta.2) (2023-09-06)


### Bug Fixes

* export TestResult and Suite types ([#786](https://github.com/gemini-testing/hermione/issues/786)) ([0d24037](https://github.com/gemini-testing/hermione/commit/0d2403764d5f292826e01a061c019a8b32bb39f7))
* ignore ProtocolError unhandled rejections ([bf80946](https://github.com/gemini-testing/hermione/commit/bf8094658e2469b3e5cf9313b584c9d1e4d324b3))
* system.debug config field ([4f3e01c](https://github.com/gemini-testing/hermione/commit/4f3e01cf5c61021e13b7f70b2041fe938dfe6929))
* use exact version of webdriverio@8.13.4 ([f7ea267](https://github.com/gemini-testing/hermione/commit/f7ea267decebc00397276d999694532bb2aabfa4))

## [8.0.0-beta.1](https://github.com/gemini-testing/hermione/compare/v8.0.0-beta.0...v8.0.0-beta.1) (2023-07-04)


### Bug Fixes

* do not reinit cached browser session in worker ([761dcb8](https://github.com/gemini-testing/hermione/commit/761dcb897969ac45296b54dad42e0a55ab15efc8))

## [8.0.0-beta.0](https://github.com/gemini-testing/hermione/compare/v7.1.0...v8.0.0-beta.0) (2023-06-21)


### ⚠ BREAKING CHANGES

* package exports have changed

### Features

* re-write major parts of hermione to typescript and get rid of typings ([c02e716](https://github.com/gemini-testing/hermione/commit/c02e716d62e3acd4537b0fb5f937b1a783c15d3d))

## [7.1.0](https://github.com/gemini-testing/hermione/compare/v7.0.9...v7.1.0) (2023-06-14)


### Features

* add "headless" setting for the main 3 browsers ([#768](https://github.com/gemini-testing/hermione/issues/768)) ([0400c33](https://github.com/gemini-testing/hermione/commit/0400c33f502530ffa8a3c13207d75696fcff0325))

### [7.0.9](https://github.com/gemini-testing/hermione/compare/v7.0.8...v7.0.9) (2023-05-30)


### Bug Fixes

* **test-runner:** out of bound error on cursor reset ([687b669](https://github.com/gemini-testing/hermione/commit/687b6691a19a23d83b69501c1cc81541f25646d3))

### [7.0.8](https://github.com/gemini-testing/hermione/compare/v7.0.7...v7.0.8) (2023-05-03)


### Bug Fixes

* take into account zero height of ignore element ([d8a3afd](https://github.com/gemini-testing/hermione/commit/d8a3afdef6a5885929b5655b5caa0e70d166dcd7))

### [7.0.7](https://github.com/gemini-testing/hermione/compare/v7.0.6...v7.0.7) (2023-05-02)


### Bug Fixes

* correctly calculate "height" in device with fractional pixel ratio ([7c2e066](https://github.com/gemini-testing/hermione/commit/7c2e066b0e9e38fc8fd5a8b30438786691c67531))

### [7.0.6](https://github.com/gemini-testing/hermione/compare/v7.0.5...v7.0.6) (2023-05-02)


### Bug Fixes

* handle rare cases with unhandled rejections due to circular refs ([fb873ad](https://github.com/gemini-testing/hermione/commit/fb873adc0c3eb9f1fb7cff4572ffae0b3bc37e92))

### [7.0.5](https://github.com/gemini-testing/hermione/compare/v7.0.4...v7.0.5) (2023-04-27)


### Bug Fixes

* handle unhandled rejections with circular refs on timeout error ([8c38c66](https://github.com/gemini-testing/hermione/commit/8c38c668f3ecbdaae61f73d740fe916582713aec))

### [7.0.4](https://github.com/gemini-testing/hermione/compare/v7.0.3...v7.0.4) (2023-04-06)


### Bug Fixes

* reset cursor correctly for body with negative coords ([a0b8cd6](https://github.com/gemini-testing/hermione/commit/a0b8cd64d6cece993b801e2ea5b9c82b59163873))

### [7.0.3](https://github.com/gemini-testing/hermione/compare/v7.0.2...v7.0.3) (2023-04-04)


### Bug Fixes

* typings for browser interface ([e0f89b8](https://github.com/gemini-testing/hermione/commit/e0f89b844e0261df31123a6a55c14b4cfb9b61ad))

### [7.0.2](https://github.com/gemini-testing/hermione/compare/v7.0.1...v7.0.2) (2023-04-03)


### Bug Fixes

* show error with stack trace on call hermione.halt method ([61cfc26](https://github.com/gemini-testing/hermione/commit/61cfc269ae356c342967126faed5bd31017ccdf8))

### [7.0.1](https://github.com/gemini-testing/hermione/compare/v7.0.0...v7.0.1) (2023-03-31)


### Bug Fixes

* **halt:** termiante after timeout ends ([c340afc](https://github.com/gemini-testing/hermione/commit/c340afc62056fb9f054e1760d2881c9486eb2dd9))

## [7.0.0](https://github.com/gemini-testing/hermione/compare/v6.1.1...v7.0.0) (2023-03-30)


### ⚠ BREAKING CHANGES

* - test.id() -> test.id
- suite.id() -> suite.id
* terminate tests execution on unhandled rejections
* node versions less than 16.0.0 are no longer supported

### Features

* add ability to write test steps ([e7171b2](https://github.com/gemini-testing/hermione/commit/e7171b28df0bbe71e395c0c812939287e443dac9))
* add logs timestamp ([3745c7d](https://github.com/gemini-testing/hermione/commit/3745c7dcc9d5bef28f317bd97bad119df4788b17))
* bump webdriverio from 7 to 8 ([4d98965](https://github.com/gemini-testing/hermione/commit/4d9896543f33fe9917b34b1eeddf71be64d8c307))
* do not pass browser id on file events ([e7cdb05](https://github.com/gemini-testing/hermione/commit/e7cdb050e8de0cf8d8df97d488a99b93ce2b8ffd))
* do not use browserId as esmDecorator ([4d81dfb](https://github.com/gemini-testing/hermione/commit/4d81dfbe421a62cfe9a55515d55574762f962bdb))
* drop node versions less than 16 ([01d53ec](https://github.com/gemini-testing/hermione/commit/01d53ec2b89322f4f6dd78e824e13c27a693beb6))
* make id a plain property ([fcdea03](https://github.com/gemini-testing/hermione/commit/fcdea03131e1c46c148e957b0f70dee8a55431df))
* move to mocha upstream ([2b1f0ef](https://github.com/gemini-testing/hermione/commit/2b1f0efae978dcf37c896366eeb8bb3521bb4765))
* read test files in master only once ([1cb6b0c](https://github.com/gemini-testing/hermione/commit/1cb6b0c1b2e1cc5ae6e91d781c201ccb801b2d09))
* remove runnable type property ([8ad298f](https://github.com/gemini-testing/hermione/commit/8ad298fee4befdad511a46ff5fd155f32ef2a541))
* support tests and config on typescript ([c5f933d](https://github.com/gemini-testing/hermione/commit/c5f933df01cce6c88ad970fef430ad17aa411fc1))
* use own test/suite/hook objects ([1384001](https://github.com/gemini-testing/hermione/commit/13840017d5203b43e3ae9bcb04f11e1460288680))


### Bug Fixes

* call BrowserTestParser methods correctly in workers ([c46ba8f](https://github.com/gemini-testing/hermione/commit/c46ba8fc6cb745f7e994d2cf3371439d31ec2044))
* correctly screen elements on device with fractional pixel ratio ([7b153d9](https://github.com/gemini-testing/hermione/commit/7b153d95eb9867e6340d264a048dda812e7db8fd))
* do not swallow errors in hermione config ([e262fae](https://github.com/gemini-testing/hermione/commit/e262fae9046a67eea6431dedddd017b2a72e7d7e))
* handle unhandled rejections ([03676b3](https://github.com/gemini-testing/hermione/commit/03676b32a4d6b8c161c34992b986041c63a05335))
* temporary overwrite "scrollIntoView" command with bug ([2fb4474](https://github.com/gemini-testing/hermione/commit/2fb4474bd169c85f555569b79d0a33fd674d7141))
* use suite position in file instead of global position to generate id ([fd3716a](https://github.com/gemini-testing/hermione/commit/fd3716a3c03aab3a2362da6a9ba997a90aec9c1d))
* use undefined as a default value for browserVersion and browserId properties ([ddfe85f](https://github.com/gemini-testing/hermione/commit/ddfe85f0c600370f1d7f6b0ed04616a656e33fbc))

### [6.1.1](https://github.com/gemini-testing/hermione/compare/v6.1.0...v6.1.1) (2023-01-30)

### [6.0.3](https://github.com/gemini-testing/hermione/compare/v6.0.2...v6.0.3) (2023-01-20)


### Bug Fixes

* remove child nodes when parent leaves callstack ([8fade7b](https://github.com/gemini-testing/hermione/commit/8fade7b2f43aef23e6cec5b6568e80d48da3d05c))

### [6.0.2](https://github.com/gemini-testing/hermione/compare/v6.0.1...v6.0.2) (2023-01-11)


### Bug Fixes

* add err field to test result ([5f6dbe4](https://github.com/gemini-testing/hermione/commit/5f6dbe4811389d1da92decbbeedb5a59553b4c06))
* change error throwing on not existing element ([16dea03](https://github.com/gemini-testing/hermione/commit/16dea0320ba85c42f207c7c4cd6c0fd773897f2b))
* throw error on invalid reference ([7b74f1b](https://github.com/gemini-testing/hermione/commit/7b74f1b04cf7977d3eabdb930717de08533d5fe9))

### [6.0.1](https://github.com/gemini-testing/hermione/compare/v6.0.0...v6.0.1) (2023-01-09)


### Bug Fixes

* use strict version of webdriverio ([a111f9b](https://github.com/gemini-testing/hermione/commit/a111f9b8f853660eda4aa631b7f8e0c0e4c21e6d))

## [6.0.0](https://github.com/gemini-testing/hermione/compare/v5.6.1...v6.0.0) (2022-12-21)


### ⚠ BREAKING CHANGES

* node versions less than 14.0.0 are no longer supported

### Features

* add "browserWSEndpoint" to be able to change ws enpoint ([57c0a06](https://github.com/gemini-testing/hermione/commit/57c0a06422c137c4eeaf279646896a1aa1fb2629))
* drop node versions less than 14 ([fad5815](https://github.com/gemini-testing/hermione/commit/fad58157fd12908195cef05d37c6c714f4f0148b))


### Bug Fixes

* callback type for "it" and hooks ([57071e6](https://github.com/gemini-testing/hermione/commit/57071e66528d5cdf9f48baaff7e92ec504cd7d17))

### [5.6.1](https://github.com/gemini-testing/hermione/compare/v5.6.0...v5.6.1) (2022-12-13)


### Bug Fixes

* **existing-browser:** do not pass unnecessary options ([451d23a](https://github.com/gemini-testing/hermione/commit/451d23ad59f90f1cc7e112015d5f4f1d57915123))
* **existing-browser:** fix request and response custom transforming ([714ddb9](https://github.com/gemini-testing/hermione/commit/714ddb93c97c325ec7e8caca134c15da22e18fb4))

## [5.6.0](https://github.com/gemini-testing/hermione/compare/v5.5.2...v5.6.0) (2022-12-06)


### Features

* add built-in assert library ([01ac6de](https://github.com/gemini-testing/hermione/commit/01ac6de407f6f1926e4a03ff3917a099526db978))


### Bug Fixes

* fill tests cache synchronously in workers ([b3b96d3](https://github.com/gemini-testing/hermione/commit/b3b96d3eef34f3da66357fabf1a051f7bcd9d64a))

### [5.5.2](https://github.com/gemini-testing/hermione/compare/v5.5.1...v5.5.2) (2022-11-23)

### [5.5.1](https://github.com/gemini-testing/hermione/compare/v5.5.0...v5.5.1) (2022-11-21)

## [5.5.0](https://github.com/gemini-testing/hermione/compare/v5.4.1...v5.5.0) (2022-11-21)


### Features

* **assert-view:** add waitForExist ([4d20b5c](https://github.com/gemini-testing/hermione/commit/4d20b5c7da1ee1c7245c7a98104f54eff5f85597))

### [5.4.1](https://github.com/gemini-testing/hermione/compare/v5.4.0...v5.4.1) (2022-11-15)


### Bug Fixes

* **devtools:** do not use cache for browsers ([bf5afb0](https://github.com/gemini-testing/hermione/commit/bf5afb0204eb232fd9c8758b7353290c508c45ae))
* **screenshot:** handle viewport overflow properly ([2142cd8](https://github.com/gemini-testing/hermione/commit/2142cd8ff4ef5cb65dc87af5e0a144225bd8137a))

## [5.4.0](https://github.com/gemini-testing/hermione/compare/v5.3.1...v5.4.0) (2022-11-08)


### Features

* esm modules support ([5fc3272](https://github.com/gemini-testing/hermione/commit/5fc3272fc24da88315d0298c9212d6ed13615f61))
* load test files asynchronously ([026e3d8](https://github.com/gemini-testing/hermione/commit/026e3d8f16df2d89128f6fa66c1ad9ea71cfecad))
* read tests sequentially in worker ([78e8485](https://github.com/gemini-testing/hermione/commit/78e84854ee334242e6867dddc41bcb07a641f233))


### Bug Fixes

* migrate png-img -> sharp ([35e9429](https://github.com/gemini-testing/hermione/commit/35e942918308279b4d6f552092d99e151eac271d))

### [5.3.1](https://github.com/gemini-testing/hermione/compare/v5.3.0...v5.3.1) (2022-10-11)


### Bug Fixes

* update png-img to 5.0.1 with windows build fix ([f3a00d1](https://github.com/gemini-testing/hermione/commit/f3a00d189c60cab571473c95cfd02bd3157c2c5a))

## [5.3.0](https://github.com/gemini-testing/hermione/compare/v5.2.2...v5.3.0) (2022-10-10)


### Features

* merge gemini-core ([0760792](https://github.com/gemini-testing/hermione/commit/07607922d4ec81a7c73382163f013678db76c1f2))
* update looks-same ([e9ac36d](https://github.com/gemini-testing/hermione/commit/e9ac36d83250e6370b32d91b212f3b9d02404d65))
* update png-img ([01712eb](https://github.com/gemini-testing/hermione/commit/01712eb8d0da1230f541cc88fb7610c1e8804b88))

### [5.2.2](https://github.com/gemini-testing/hermione/compare/v5.2.1...v5.2.2) (2022-09-09)


### Bug Fixes

* vulnerabilities ([7c3e942](https://github.com/gemini-testing/hermione/commit/7c3e942292d3eab9f84a420246343134f2eabf94))

<a name="5.2.0"></a>
# [5.2.0](https://github.com/gemini-testing/hermione/compare/v5.1.2...v5.2.0) (2022-08-30)


### Features

* add element's assertView method ([54724f7](https://github.com/gemini-testing/hermione/commit/54724f7))



<a name="5.1.2"></a>
## [5.1.2](https://github.com/gemini-testing/hermione/compare/v5.1.1...v5.1.2) (2022-08-29)


### Bug Fixes

* **types:** set correct type for "sets" field in config ([0164875](https://github.com/gemini-testing/hermione/commit/0164875))



<a name="5.1.1"></a>
## [5.1.1](https://github.com/gemini-testing/hermione/compare/v5.1.0...v5.1.1) (2022-08-19)


### Bug Fixes

* 'this' pointer in custom commands ([1a2b486](https://github.com/gemini-testing/hermione/commit/1a2b486))



<a name="5.1.0"></a>
# [5.1.0](https://github.com/gemini-testing/hermione/compare/v5.0.1...v5.1.0) (2022-08-15)


### Features

* add getConfig to the browser instance ([30f579e](https://github.com/gemini-testing/hermione/commit/30f579e))
* update gemini-core to the version with png-img[@4](https://github.com/4) ([58f3da8](https://github.com/gemini-testing/hermione/commit/58f3da8))



<a name="5.0.1"></a>
## [5.0.1](https://github.com/gemini-testing/hermione/compare/v5.0.0...v5.0.1) (2022-06-29)


### Bug Fixes

* **types:** add 'headers' property to config ([a0061d2](https://github.com/gemini-testing/hermione/commit/a0061d2))



<a name="5.0.0"></a>
# [5.0.0](https://github.com/gemini-testing/hermione/compare/v4.9.1...v5.0.0) (2022-06-11)


### Bug Fixes

* change some default values to more commonly used ([40b8343](https://github.com/gemini-testing/hermione/commit/40b8343))
* do not passthrough parser events via TestParserApi ([5f26c80](https://github.com/gemini-testing/hermione/commit/5f26c80))
* remove deprecated options ([cf1d69f](https://github.com/gemini-testing/hermione/commit/cf1d69f))
* remove unused "teamcity" reporter ([56a9293](https://github.com/gemini-testing/hermione/commit/56a9293))
* use "-r" option for require module and not for "--reporter" ([ca35198](https://github.com/gemini-testing/hermione/commit/ca35198))


### Features

* add "jsonl" reporter ([08140fd](https://github.com/gemini-testing/hermione/commit/08140fd))
* add ability to redirect output of reporter to the file ([066c590](https://github.com/gemini-testing/hermione/commit/066c590))


### BREAKING CHANGES

* - change default value for "saveHistory" option from "false" to "true"
- change default value for "antialiasingTolerance" option from "0" to "4"
- change default value for "compositeImage" option from "false" to "true"
- change default value for "takeScreenshotOnFails.assertViewFail" option from "false" to "true"
- change default value for "takeScreenshotOnFailsMode" option from "viewport" to "fullpage"
- change default value for "httpTimeout" option from "90000" to "30000"
- change default value for "pageLoadTimeout" option from "300000" to " 20000"
- change default value for "sessionQuitTimeout" option from "90000" to "5000"
- change default value for "takeScreenshotOnFailsTimeout" option from "90000" to "5000"
* option "-r" is no longer sets the specified reporter, now it uses for require module
* remove deprecated options: "screenshotOnReject" and "screenshotOnRejectTimeout"
* reporters specified as function and used through programmatic API must have a static create method for initialization
* "teamcity" reporter is no longer supported, use "hermione-teamcity-reporter" plugin instead
* testParserApi object passed on BEFORE_FILE_READ event is no longer an EventEmitter



<a name="4.9.1"></a>
## [4.9.1](https://github.com/gemini-testing/hermione/compare/v4.9.0...v4.9.1) (2022-05-24)



<a name="4.9.0"></a>
# [4.9.0](https://github.com/gemini-testing/hermione/compare/v4.8.0...v4.9.0) (2022-05-24)


### Features

* pass browser into test as an argument ([7b5d655](https://github.com/gemini-testing/hermione/commit/7b5d655))



<a name="4.8.0"></a>
## [4.8.0](https://github.com/gemini-testing/hermione/compare/v4.7.8...v4.8.0) (2022-03-22)

### Features

* **worker/test-runner:**  take the error screenshot on every test fail ([2199e0b5](https://github.com/gemini-testing/hermione/commit/2199e0b57ece8e0f46d0f7be141c44827f417d27))

### Tests

* **worker/test-runner:**  add new and remove unnecessary unit tests ([637654ae](https://github.com/gemini-testing/hermione/commit/637654aed892d14b57a10b907cf83cf7066528a1))


<a name="4.7.8"></a>
## [4.7.8](https://github.com/gemini-testing/hermione/compare/v4.7.7...v4.7.8) (2022-03-04)



<a name="4.7.7"></a>
## [4.7.7](https://github.com/gemini-testing/hermione/compare/v4.7.6...v4.7.7) (2022-02-07)


### Bug Fixes

* update gemini-core to 6.3.6 ([452bc69](https://github.com/gemini-testing/hermione/commit/452bc69))



<a name="4.7.6"></a>
## [4.7.6](https://github.com/gemini-testing/hermione/compare/v4.7.5...v4.7.6) (2022-01-26)


### Bug Fixes

* move mocha and wdio types from dev deps to deps ([c23a0b9](https://github.com/gemini-testing/hermione/commit/c23a0b9))



<a name="4.7.5"></a>
## [4.7.5](https://github.com/gemini-testing/hermione/compare/v4.7.4...v4.7.5) (2021-12-15)



<a name="4.7.4"></a>
## [4.7.4](https://github.com/gemini-testing/hermione/compare/v4.7.3...v4.7.4) (2021-11-24)


### Bug Fixes

* correct logic for running it.only/describe.only ([b448222](https://github.com/gemini-testing/hermione/commit/b448222))



<a name="4.7.2"></a>
## [4.7.2](https://github.com/gemini-testing/hermione/compare/v4.7.1...v4.7.2) (2021-11-11)


### Bug Fixes

* up version gemini-core to support Node 16 ([6b5af5d](https://github.com/gemini-testing/hermione/commit/6b5af5d))



<a name="4.7.1"></a>
## [4.7.1](https://github.com/gemini-testing/hermione/compare/v4.7.0...v4.7.1) (2021-11-08)



<a name="4.7.0"></a>
# [4.7.0](https://github.com/gemini-testing/hermione/compare/v4.6.4...v4.7.0) (2021-11-08)


### Features

* add "startTime" field to test result in order to use in plugins ([9dfb5ed](https://github.com/gemini-testing/hermione/commit/9dfb5ed))



<a name="4.6.4"></a>
## [4.6.4](https://github.com/gemini-testing/hermione/compare/v4.6.3...v4.6.4) (2021-10-15)


### Bug Fixes

* throw error when there are no tests found ([ec9eed1](https://github.com/gemini-testing/hermione/commit/ec9eed1))



<a name="4.6.3"></a>
## [4.6.3](https://github.com/gemini-testing/hermione/compare/v4.6.2...v4.6.3) (2021-10-13)


### Bug Fixes

* bug with incorrect work in internet explorer ([6c8924f](https://github.com/gemini-testing/hermione/commit/6c8924f))



<a name="4.6.2"></a>
## [4.6.2](https://github.com/gemini-testing/hermione/compare/v4.6.1...v4.6.2) (2021-10-13)


### Bug Fixes

* add ability to take screenshot if element is out of the bounds ([6c55e74](https://github.com/gemini-testing/hermione/commit/6c55e74))



<a name="4.6.1"></a>
## [4.6.1](https://github.com/gemini-testing/hermione/compare/v4.6.0...v4.6.1) (2021-10-13)


### Bug Fixes

* incorrect work of "grep" option ([0c355fe](https://github.com/gemini-testing/hermione/commit/0c355fe))



<a name="4.6.0"></a>
# [4.6.0](https://github.com/gemini-testing/hermione/compare/v4.5.0...v4.6.0) (2021-10-12)


### Features

* add ability to use xpath selectors in "assertView" command ([d399b5f](https://github.com/gemini-testing/hermione/commit/d399b5f))



<a name="4.5.0"></a>
# [4.5.0](https://github.com/gemini-testing/hermione/compare/v4.4.4...v4.5.0) (2021-10-11)


### Features

* move from mocha[@2](https://github.com/2).4.5 to [@gemini](https://github.com/gemini)-testing/mocha[@9](https://github.com/9).1.5 ([c181f42](https://github.com/gemini-testing/hermione/commit/c181f42))



<a name="4.4.4"></a>
## [4.4.4](https://github.com/gemini-testing/hermione/compare/v4.4.3...v4.4.4) (2021-10-01)


### Bug Fixes

* correct work of "patternsOnReject" ([a936006](https://github.com/gemini-testing/hermione/commit/a936006))



<a name="4.4.3"></a>
## [4.4.3](https://github.com/gemini-testing/hermione/compare/v4.4.2...v4.4.3) (2021-09-17)



<a name="4.4.2"></a>
## [4.4.2](https://github.com/gemini-testing/hermione/compare/v4.4.1...v4.4.2) (2021-09-09)



<a name="4.4.1"></a>
## [4.4.1](https://github.com/gemini-testing/hermione/compare/v4.4.0...v4.4.1) (2021-09-03)


### Bug Fixes

* reinit browser in worker with his session options ([585f5fa](https://github.com/gemini-testing/hermione/commit/585f5fa))



<a name="4.4.0"></a>
# [4.4.0](https://github.com/gemini-testing/hermione/compare/v4.3.0...v4.4.0) (2021-08-26)


### Bug Fixes

* throw error when there is no "body" when resetting cursor pos ([b7e8925](https://github.com/gemini-testing/hermione/commit/b7e8925))


### Features

* reuse session options in worker from master ([1a50a87](https://github.com/gemini-testing/hermione/commit/1a50a87))



<a name="4.3.0"></a>
# [4.3.0](https://github.com/gemini-testing/hermione/compare/v4.2.2...v4.3.0) (2021-08-24)


### Features

* hermione constructor can take configuration as an object ([1666a29](https://github.com/gemini-testing/hermione/commit/1666a29))



<a name="4.2.2"></a>
## [4.2.2](https://github.com/gemini-testing/hermione/compare/v4.2.1...v4.2.2) (2021-08-23)


### Bug Fixes

* errors in typings ([49e1117](https://github.com/gemini-testing/hermione/commit/49e1117))



<a name="4.2.1"></a>
## [4.2.1](https://github.com/gemini-testing/hermione/compare/v4.2.0...v4.2.1) (2021-08-17)



<a name="4.1.4"></a>
## [4.1.4](https://github.com/gemini-testing/hermione/compare/v4.1.3...v4.1.4) (2021-07-07)


### Bug Fixes

* **ie11:** execute script correctly on scroll page ([6481824](https://github.com/gemini-testing/hermione/commit/6481824))



<a name="4.1.3"></a>
## [4.1.3](https://github.com/gemini-testing/hermione/compare/v4.1.2...v4.1.3) (2021-07-06)


### Bug Fixes

* do not wrap system commands ([47c9776](https://github.com/gemini-testing/hermione/commit/47c9776))



<a name="4.1.2"></a>
## [4.1.2](https://github.com/gemini-testing/hermione/compare/v4.1.1...v4.1.2) (2021-07-06)



<a name="4.1.1"></a>
## [4.1.1](https://github.com/gemini-testing/hermione/compare/v4.1.0...v4.1.1) (2021-07-02)


### Bug Fixes

* **attach:** pass "requestedCapabilities" in order to using CDP in CI ([dbff2a5](https://github.com/gemini-testing/hermione/commit/dbff2a5))



<a name="4.1.0"></a>
# [4.1.0](https://github.com/gemini-testing/hermione/compare/v4.0.0...v4.1.0) (2021-06-28)


### Features

* ability to scroll page by passed selector ([7307ae1](https://github.com/gemini-testing/hermione/commit/7307ae1))



<a name="4.0.0"></a>
# [4.0.0](https://github.com/gemini-testing/hermione/compare/v4.0.0-alpha.9...v4.0.0) (2021-06-28)

### BREAKING CHANGES
* node versions less than 12.0.0 are no longer supported
* move to latest version of webdriverio (7.x) from our fork
* remove browser options: "screenshotPath", "w3cCompatible"
* custom implementation of commands history

### Features

* Implemented commands-history ([b4c1531](https://github.com/gemini-testing/hermione/commit/b4c1531))
* drop node versions less than 12 ([48fb22b](https://github.com/gemini-testing/hermione/commit/48fb22b))
* update wdio[@4](https://github.com/4) to wdio[@7](https://github.com/7) ([66057b4](https://github.com/gemini-testing/hermione/commit/66057b4))

### Bug Fixes

* remove features related to wdio native history ([8205bf3](https://github.com/gemini-testing/hermione/commit/8205bf3))
* set screenshotMode to viewport on android browsers ([326f5a7](https://github.com/gemini-testing/hermione/commit/326f5a7))
* ability to run tests using "devtools" protocol ([85bc868](https://github.com/gemini-testing/hermione/commit/85bc868))
* **test-collection:** compare test titles with trim ([e245993](https://github.com/gemini-testing/hermione/commit/e245993))
* **worker:** load external modules from "--require" option ([1abb66a](https://github.com/gemini-testing/hermione/commit/1abb66a))
* use new typings from webdriverio ([63d1a5a](https://github.com/gemini-testing/hermione/commit/63d1a5a))
* set default port "4444" if it is not specified in "gridUrl" ([5dae3c7](https://github.com/gemini-testing/hermione/commit/5dae3c7))
* do not fall if port is not specified in "gridUrl" ([4e6f49e](https://github.com/gemini-testing/hermione/commit/4e6f49e))
* set default port "4444" if it is not specified in "gridUrl" ([5de53aa](https://github.com/gemini-testing/hermione/commit/5de53aa))
* add error catch on set page load timeout for edge with w3c support ([f7e438b](https://github.com/gemini-testing/hermione/commit/f7e438b))
* error in expectation of orientation change ([3c8b21d](https://github.com/gemini-testing/hermione/commit/3c8b21d))
* reuse session caps in worker from master ([5c70fe0](https://github.com/gemini-testing/hermione/commit/5c70fe0))
* call "getUrl" if url is not passed in "url" wrapper ([24dbd18](https://github.com/gemini-testing/hermione/commit/24dbd18))
* get body width only if it is necessary in "setOrientation" wrapper ([a75655b](https://github.com/gemini-testing/hermione/commit/a75655b))
* removed temp hack with error catching on set page load timeout ([073cac7](https://github.com/gemini-testing/hermione/commit/073cac7))


<a name="3.11.0"></a>
# [3.11.0](https://github.com/gemini-testing/hermione/compare/v3.10.4...v3.11.0) (2021-02-25)


### Features

* added urlTimeout option to config ([82856d9](https://github.com/gemini-testing/hermione/commit/82856d9))



<a name="3.10.4"></a>
## [3.10.4](https://github.com/gemini-testing/hermione/compare/v3.10.3...v3.10.4) (2021-02-18)


### Bug Fixes

* set timeout for execution screenshot on reject ([dd73f3e](https://github.com/gemini-testing/hermione/commit/dd73f3e))



<a name="3.10.3"></a>
## [3.10.3](https://github.com/gemini-testing/hermione/compare/v3.10.2...v3.10.3) (2021-02-03)



<a name="3.10.2"></a>
## [3.10.2](https://github.com/gemini-testing/hermione/compare/v3.10.1...v3.10.2) (2021-01-14)



<a name="3.10.1"></a>
## [3.10.1](https://github.com/gemini-testing/hermione/compare/v3.10.0...v3.10.1) (2020-12-14)


### Bug Fixes

* handle cases when sets from 'CLI' were not been passed ([1054f67](https://github.com/gemini-testing/hermione/commit/1054f67))



<a name="3.10.0"></a>
# [3.10.0](https://github.com/gemini-testing/hermione/compare/v3.9.1...v3.10.0) (2020-12-14)


### Features

* add 'HERMIONE_SETS' environment variable ([eeca127](https://github.com/gemini-testing/hermione/commit/eeca127))



<a name="3.9.1"></a>
## [3.9.1](https://github.com/gemini-testing/hermione/compare/v3.9.0...v3.9.1) (2020-11-13)



<a name="3.9.0"></a>
# [3.9.0](https://github.com/gemini-testing/hermione/compare/v3.8.7...v3.9.0) (2020-09-27)


### Features

* added 'hasBrowserVersionOverwriten' property for test ([c0280ce](https://github.com/gemini-testing/hermione/commit/c0280ce))



<a name="3.8.7"></a>
## [3.8.7](https://github.com/gemini-testing/hermione/compare/v3.8.6...v3.8.7) (2020-09-25)



<a name="3.8.6"></a>
## [3.8.6](https://github.com/gemini-testing/hermione/compare/v3.8.5...v3.8.6) (2020-09-18)


### Bug Fixes

* even more proper lists ([4a078e8](https://github.com/gemini-testing/hermione/commit/4a078e8))
* more proper lists ([afca4f4](https://github.com/gemini-testing/hermione/commit/afca4f4))
* proper headers in readme ([ac49782](https://github.com/gemini-testing/hermione/commit/ac49782))



<a name="3.8.5"></a>
## [3.8.5](https://github.com/gemini-testing/hermione/compare/v3.8.4...v3.8.5) (2020-08-23)



<a name="3.8.4"></a>
## [3.8.4](https://github.com/gemini-testing/hermione/compare/v3.8.3...v3.8.4) (2020-08-12)


### Bug Fixes

* up gemini-core version ([c7dda90](https://github.com/gemini-testing/hermione/commit/c7dda90))



<a name="3.8.3"></a>
## [3.8.3](https://github.com/gemini-testing/hermione/compare/v3.8.2...v3.8.3) (2020-08-11)


### Bug Fixes

* find browser in cache according to a browser version ([12df805](https://github.com/gemini-testing/hermione/commit/12df805))



<a name="3.8.2"></a>
## [3.8.2](https://github.com/gemini-testing/hermione/compare/v3.8.1...v3.8.2) (2020-08-07)


### Bug Fixes

* stringify safely object arguments in command history ([eb87464](https://github.com/gemini-testing/hermione/commit/eb87464))



<a name="3.8.1"></a>
## [3.8.1](https://github.com/gemini-testing/hermione/compare/v3.8.0...v3.8.1) (2020-07-17)


### Bug Fixes

* determine browser versions before run ([e73cce6](https://github.com/gemini-testing/hermione/commit/e73cce6))



<a name="3.8.0"></a>
# [3.8.0](https://github.com/gemini-testing/hermione/compare/v3.7.1...v3.8.0) (2020-07-08)


### Features

* Implemented browser version assert ([d496740](https://github.com/gemini-testing/hermione/commit/d496740))
* Store a browser version in a meta object of a test-case ([f93e3bf](https://github.com/gemini-testing/hermione/commit/f93e3bf))



<a name="3.7.1"></a>
## [3.7.1](https://github.com/gemini-testing/hermione/compare/v3.7.0...v3.7.1) (2020-07-02)



<a name="3.7.0"></a>
# [3.7.0](https://github.com/gemini-testing/hermione/compare/v3.6.0...v3.7.0) (2020-07-02)


### Features

* allow to save command history on any error ([de078a3](https://github.com/gemini-testing/hermione/commit/de078a3))



<a name="3.6.0"></a>
# [3.6.0](https://github.com/gemini-testing/hermione/compare/v3.5.3...v3.6.0) (2020-06-24)


### Features

* Ability to run tests in different versions of browsers ([d7df135](https://github.com/gemini-testing/hermione/commit/d7df135))



<a name="3.5.3"></a>
## [3.5.3](https://github.com/gemini-testing/hermione/compare/v3.5.2...v3.5.3) (2020-06-20)


### Bug Fixes

* hermione typings ([8a61ee6](https://github.com/gemini-testing/hermione/commit/8a61ee6))



<a name="3.5.2"></a>
## [3.5.2](https://github.com/gemini-testing/hermione/compare/v3.5.1...v3.5.2) (2020-06-16)



<a name="3.5.1"></a>
## [3.5.1](https://github.com/gemini-testing/hermione/compare/v3.5.0...v3.5.1) (2020-06-16)



<a name="3.5.0"></a>
# [3.5.0](https://github.com/gemini-testing/hermione/compare/v3.4.0...v3.5.0) (2020-06-16)


### Features

* add subscriptions to parser events for TestParserAPI ([1be789a](https://github.com/gemini-testing/hermione/commit/1be789a))



<a name="3.4.0"></a>
# [3.4.0](https://github.com/gemini-testing/hermione/compare/v3.3.1...v3.4.0) (2020-06-01)


### Features

* add browser option "waitOrientationChange" ([e15b3c1](https://github.com/gemini-testing/hermione/commit/e15b3c1))



<a name="3.3.1"></a>
## [3.3.1](https://github.com/gemini-testing/hermione/compare/v3.3.0...v3.3.1) (2020-05-09)



<a name="3.3.0"></a>
# [3.3.0](https://github.com/gemini-testing/hermione/compare/v3.2.0...v3.3.0) (2020-04-29)


### Features

* add cli option "--require" to load external modules ([c93e652](https://github.com/gemini-testing/hermione/commit/c93e652))



<a name="3.2.0"></a>
# [3.2.0](https://github.com/gemini-testing/hermione/compare/v3.1.0...v3.2.0) (2020-04-25)


### Features

* add ability to change file extensions ([ffb5449](https://github.com/gemini-testing/hermione/commit/ffb5449))



<a name="3.1.0"></a>
# [3.1.0](https://github.com/gemini-testing/hermione/compare/v3.0.1...v3.1.0) (2020-03-29)


### Features

* add command history to error for timedout tests ([8023d48](https://github.com/gemini-testing/hermione/commit/8023d48))



<a name="3.0.1"></a>
## [3.0.1](https://github.com/gemini-testing/hermione/compare/v3.0.0...v3.0.1) (2020-03-11)



<a name="3.0.0"></a>
# [3.0.0](https://github.com/gemini-testing/hermione/compare/v2.13.6...v3.0.0) (2020-01-28)


### Features

* change options in "assertView" command ([763be83](https://github.com/gemini-testing/hermione/commit/763be83))


### BREAKING CHANGES

* option "allowViewportOverflow" now allows to overflow bottom viewport bound

- add browser option "assertViewOpts" which is used as default options inside "assertView"
- add ability to set "compositeImage"
- add ability to set "antialiasingTolerance"
- add ability to set "captureElementFromTop" in order for more precise control of capture image
- update gemini-core from 4.0.0 to 5.0.0



<a name="2.13.6"></a>
## [2.13.6](https://github.com/gemini-testing/hermione/compare/v2.13.5...v2.13.6) (2020-01-21)


### Bug Fixes

* create browser pool after emit INIT event ([4518b30](https://github.com/gemini-testing/hermione/commit/4518b30))



<a name="2.13.5"></a>
## [2.13.5](https://github.com/gemini-testing/hermione/compare/v2.13.4...v2.13.5) (2019-12-17)


### Bug Fixes

* never use browser session again if it fails on initializition ([1036969](https://github.com/gemini-testing/hermione/commit/1036969))



<a name="2.13.4"></a>
## [2.13.4](https://github.com/gemini-testing/hermione/compare/v2.13.3...v2.13.4) (2019-12-03)


### Bug Fixes

* prepareScreenshot method should throw error from browser ([10164db](https://github.com/gemini-testing/hermione/commit/10164db))



<a name="2.13.3"></a>
## [2.13.3](https://github.com/gemini-testing/hermione/compare/v2.13.2...v2.13.3) (2019-11-25)


### Bug Fixes

* increment stats for each test result ([cdb1ac3](https://github.com/gemini-testing/hermione/commit/cdb1ac3))



<a name="2.13.2"></a>
## [2.13.2](https://github.com/gemini-testing/hermione/compare/v2.13.1...v2.13.2) (2019-11-25)


### Bug Fixes

* use sessionId in the name of free browser event ([782305e](https://github.com/gemini-testing/hermione/commit/782305e))



<a name="2.13.1"></a>
## [2.13.1](https://github.com/gemini-testing/hermione/compare/v2.13.0...v2.13.1) (2019-10-15)


### Bug Fixes

* **assert-view:** missed hermioneCtx on assertView execution ([8facf53](https://github.com/gemini-testing/hermione/commit/8facf53))



<a name="2.13.0"></a>
# [2.13.0](https://github.com/gemini-testing/hermione/compare/v2.12.6...v2.13.0) (2019-10-10)


### Features

* allow override testTimeout for specific tests ([3d3e3d1](https://github.com/gemini-testing/hermione/commit/3d3e3d1))



<a name="2.12.6"></a>
## [2.12.6](https://github.com/gemini-testing/hermione/compare/v2.12.5...v2.12.6) (2019-08-20)



<a name="2.12.5"></a>
## [2.12.5](https://github.com/gemini-testing/hermione/compare/v2.12.4...v2.12.5) (2019-08-19)



<a name="2.12.4"></a>
## [2.12.4](https://github.com/gemini-testing/hermione/compare/v2.12.3...v2.12.4) (2019-08-08)


### Bug Fixes

* mark session as broken on cursor reset error ([9083e8d](https://github.com/gemini-testing/hermione/commit/9083e8d))



<a name="2.12.3"></a>
## [2.12.3](https://github.com/gemini-testing/hermione/compare/v2.12.2...v2.12.3) (2019-07-30)


### Bug Fixes

* always release browser ([cdbb742](https://github.com/gemini-testing/hermione/commit/cdbb742))



<a name="2.12.2"></a>
## [2.12.2](https://github.com/gemini-testing/hermione/compare/v2.12.1...v2.12.2) (2019-07-25)


### Bug Fixes

* make test.id looks like a property ([9964432](https://github.com/gemini-testing/hermione/commit/9964432))



<a name="2.12.1"></a>
## [2.12.1](https://github.com/gemini-testing/hermione/compare/v2.12.0...v2.12.1) (2019-07-25)


### Bug Fixes

* test frees random browser ([f1419e6](https://github.com/gemini-testing/hermione/commit/f1419e6))



<a name="2.12.0"></a>
# [2.12.0](https://github.com/gemini-testing/hermione/compare/v2.11.2...v2.12.0) (2019-07-24)


### Features

* release browser before firing any test finish event ([876510a](https://github.com/gemini-testing/hermione/commit/876510a))



<a name="2.11.2"></a>
## [2.11.2](https://github.com/gemini-testing/hermione/compare/v2.11.1...v2.11.2) (2019-07-23)



<a name="2.11.0"></a>
# [2.11.0](https://github.com/gemini-testing/hermione/compare/v2.10.1...v2.11.0) (2019-07-18)


### Features

* ability to guarantee tests order after reading ([e14faef](https://github.com/gemini-testing/hermione/commit/e14faef))



<a name="2.10.1"></a>
## [2.10.1](https://github.com/gemini-testing/hermione/compare/v2.10.0...v2.10.1) (2019-07-15)


### Bug Fixes

* scrollBy using scrollTo ([95d7b06](https://github.com/gemini-testing/hermione/commit/95d7b06))



<a name="2.10.0"></a>
# [2.10.0](https://github.com/gemini-testing/hermione/compare/v2.9.0...v2.10.0) (2019-07-09)


### Features

* **sets:** add set.ignoreFiles option to ignore dirs while test finding ([53749c8](https://github.com/gemini-testing/hermione/commit/53749c8))



<a name="2.9.0"></a>
# [2.9.0](https://github.com/gemini-testing/hermione/compare/v2.8.1...v2.9.0) (2019-07-07)


### Features

* send session id on browser session events ([189faff](https://github.com/gemini-testing/hermione/commit/189faff))



<a name="2.8.1"></a>
## [2.8.1](https://github.com/gemini-testing/hermione/compare/v2.8.0...v2.8.1) (2019-06-27)


### Bug Fixes

* proxy events before workers init ([#417](https://github.com/gemini-testing/hermione/issues/417)) ([8b2456a](https://github.com/gemini-testing/hermione/commit/8b2456a))



<a name="2.8.0"></a>
# [2.8.0](https://github.com/gemini-testing/hermione/compare/v2.7.1...v2.8.0) (2019-06-26)


### Features

* add newWorkerProcess event ([#416](https://github.com/gemini-testing/hermione/issues/416)) ([3183352](https://github.com/gemini-testing/hermione/commit/3183352))



<a name="2.7.1"></a>
## [2.7.1](https://github.com/gemini-testing/hermione/compare/v2.7.0...v2.7.1) (2019-06-06)


### Bug Fixes

* logic of ignore caret option on ImageDiffError ([d44c92a](https://github.com/gemini-testing/hermione/commit/d44c92a))



<a name="2.7.0"></a>
# [2.7.0](https://github.com/gemini-testing/hermione/compare/v2.6.1...v2.7.0) (2019-05-27)


### Features

* add method 'registerWorkers' to Runner ([139e9b8](https://github.com/gemini-testing/hermione/commit/139e9b8))



<a name="2.6.1"></a>
## [2.6.1](https://github.com/gemini-testing/hermione/compare/v2.6.0...v2.6.1) (2019-05-06)


### Bug Fixes

* empty test-collection sorting ([#403](https://github.com/gemini-testing/hermione/issues/403)) ([fb87508](https://github.com/gemini-testing/hermione/commit/fb87508))



<a name="2.6.0"></a>
# [2.6.0](https://github.com/gemini-testing/hermione/compare/v2.5.0...v2.6.0) (2019-04-30)


### Features

* update wdio version ([761a417](https://github.com/gemini-testing/hermione/commit/761a417))



<a name="2.5.0"></a>
# [2.5.0](https://github.com/gemini-testing/hermione/compare/v2.4.0...v2.5.0) (2019-04-18)


### Features

* add "UPDATE_REFERENCE" event ([8c30e0f](https://github.com/gemini-testing/hermione/commit/8c30e0f))



<a name="2.4.0"></a>
# [2.4.0](https://github.com/gemini-testing/hermione/compare/v2.3.1...v2.4.0) (2019-04-04)


### Features

* add screenshotDelay option for assertView ([0907c1b](https://github.com/gemini-testing/hermione/commit/0907c1b))



<a name="2.3.1"></a>
## [2.3.1](https://github.com/gemini-testing/hermione/compare/v2.3.0...v2.3.1) (2019-04-03)


### Bug Fixes

* grep finds tests by regex and regex-like strings ([acab128](https://github.com/gemini-testing/hermione/commit/acab128))
* update runtime config before creating runner ([fc22e05](https://github.com/gemini-testing/hermione/commit/fc22e05))



<a name="2.3.0"></a>
# [2.3.0](https://github.com/gemini-testing/hermione/compare/v2.2.1...v2.3.0) (2019-03-27)


### Features

* add browser option "testTimeout" ([7835aac](https://github.com/gemini-testing/hermione/commit/7835aac))



<a name="2.2.1"></a>
## [2.2.1](https://github.com/gemini-testing/hermione/compare/v2.2.0...v2.2.1) (2019-03-20)


### Bug Fixes

* update gemini-core to 3.6.1 ([8e5ac84](https://github.com/gemini-testing/hermione/commit/8e5ac84))



<a name="2.2.0"></a>
# [2.2.0](https://github.com/gemini-testing/hermione/compare/v2.1.0...v2.2.0) (2019-03-15)


### Features

* add allowViewportOverflow option to assertView ([47bfc9f](https://github.com/gemini-testing/hermione/commit/47bfc9f))



<a name="2.1.0"></a>
# [2.1.0](https://github.com/gemini-testing/hermione/compare/v2.0.0...v2.1.0) (2019-03-13)


### Features

* add diff clusters ([1b71aae](https://github.com/gemini-testing/hermione/commit/1b71aae))



<a name="2.0.0"></a>
# [2.0.0](https://github.com/gemini-testing/hermione/compare/v1.10.0...v2.0.0) (2019-02-27)


### Bug Fixes

* forbid duplicate state names in 'assertView' within one test ([68600ff](https://github.com/gemini-testing/hermione/commit/68600ff))


### Features

* do not pass tests' statistic on 'END' event ([437aef7](https://github.com/gemini-testing/hermione/commit/437aef7))


### BREAKING CHANGES

* 'END' event handler will not recieve tests' statistic as the first argument
* test with duplicate state names in 'assertView' calls will fail with 'AssertViewError'



<a name="1.10.0"></a>
# [1.10.0](https://github.com/gemini-testing/hermione/compare/v1.9.0...v1.10.0) (2019-02-25)


### Features

* **config:** add parallelLimit option ([e116e91](https://github.com/gemini-testing/hermione/commit/e116e91))



<a name="1.9.0"></a>
# [1.9.0](https://github.com/gemini-testing/hermione/compare/v1.8.0...v1.9.0) (2019-02-19)


### Features

* **wdio:** update wdio version ([613d31a](https://github.com/gemini-testing/hermione/commit/613d31a))



<a name="1.8.0"></a>
# [1.8.0](https://github.com/gemini-testing/hermione/compare/v1.7.2...v1.8.0) (2019-02-15)


### Bug Fixes

* AssertViewError should not replace runtime error ([7e6aca4](https://github.com/gemini-testing/hermione/commit/7e6aca4))


### Features

* add sortTests for TestCollection ([02f7da8](https://github.com/gemini-testing/hermione/commit/02f7da8))
* add tolerance option to assert view command ([d87acda](https://github.com/gemini-testing/hermione/commit/d87acda))



<a name="1.7.2"></a>
## [1.7.2](https://github.com/gemini-testing/hermione/compare/v1.7.1...v1.7.2) (2019-02-12)


### Bug Fixes

* logging for unhandledRejection ([e8bb9f3](https://github.com/gemini-testing/hermione/commit/e8bb9f3))



<a name="1.7.1"></a>
## [1.7.1](https://github.com/gemini-testing/hermione/compare/v1.7.0...v1.7.1) (2019-02-07)


### Bug Fixes

* **stats:** correctly handle events happened after first getResult call ([7b9088c](https://github.com/gemini-testing/hermione/commit/7b9088c))



<a name="1.7.0"></a>
# [1.7.0](https://github.com/gemini-testing/hermione/compare/v1.6.1...v1.7.0) (2019-02-06)


### Features

* add per browser stats ([70a7b7f](https://github.com/gemini-testing/hermione/commit/70a7b7f))



<a name="1.6.1"></a>
## [1.6.1](https://github.com/gemini-testing/hermione/compare/v1.6.0...v1.6.1) (2019-02-05)


### Bug Fixes

* emitting of fail event from plugin does not fail process ([45e519e](https://github.com/gemini-testing/hermione/commit/45e519e))



<a name="1.6.0"></a>
# [1.6.0](https://github.com/gemini-testing/hermione/compare/v1.5.1...v1.6.0) (2019-02-05)


### Features

* add ability to emit test result events from plugins ([d9e2ad7](https://github.com/gemini-testing/hermione/commit/d9e2ad7))



<a name="1.5.1"></a>
## [1.5.1](https://github.com/gemini-testing/hermione/compare/v1.5.0...v1.5.1) (2019-02-01)


### Bug Fixes

* suite.id() no longer depends on parsing order ([d13d82d](https://github.com/gemini-testing/hermione/commit/d13d82d))



<a name="1.5.0"></a>
# [1.5.0](https://github.com/gemini-testing/hermione/compare/v1.4.0...v1.5.0) (2019-01-29)


### Features

* add option "buildDiffOpts" to configure building diff image ([b83e2ba](https://github.com/gemini-testing/hermione/commit/b83e2ba))



<a name="1.4.0"></a>
# [1.4.0](https://github.com/gemini-testing/hermione/compare/v1.3.1...v1.4.0) (2019-01-29)


### Features

* add 'END' event ([4491eb1](https://github.com/gemini-testing/hermione/commit/4491eb1))
* add ability not to translate events via interceptors ([243aeab](https://github.com/gemini-testing/hermione/commit/243aeab))



<a name="1.3.1"></a>
## [1.3.1](https://github.com/gemini-testing/hermione/compare/v1.3.0...v1.3.1) (2019-01-28)


### Bug Fixes

* stop escaping of special symbols in grep ([9bbb028](https://github.com/gemini-testing/hermione/commit/9bbb028))



<a name="1.3.0"></a>
# [1.3.0](https://github.com/gemini-testing/hermione/compare/v1.2.4...v1.3.0) (2019-01-24)


### Features

* use ref image from looks-same ([ff4635a](https://github.com/gemini-testing/hermione/commit/ff4635a))



<a name="1.2.4"></a>
## [1.2.4](https://github.com/gemini-testing/hermione/compare/v1.2.3...v1.2.4) (2019-01-18)


### Bug Fixes

* meta randomly does not contain 'pid' ([1e476c9](https://github.com/gemini-testing/hermione/commit/1e476c9))



<a name="1.2.3"></a>
## [1.2.3](https://github.com/gemini-testing/hermione/compare/v1.2.2...v1.2.3) (2019-01-16)


### Bug Fixes

* test meta from worker totally redefines test meta from master ([df2b97e](https://github.com/gemini-testing/hermione/commit/df2b97e))



<a name="1.2.2"></a>
## [1.2.2](https://github.com/gemini-testing/hermione/compare/v1.2.1...v1.2.2) (2019-01-10)


### Bug Fixes

* correct documentation about compare options ([543d165](https://github.com/gemini-testing/hermione/commit/543d165))
* do not fall by memory in looks-same ([6f11eda](https://github.com/gemini-testing/hermione/commit/6f11eda))



<a name="1.2.1"></a>
## [1.2.1](https://github.com/gemini-testing/hermione/compare/v1.2.0...v1.2.1) (2018-12-26)


### Bug Fixes

* use gemini-core with stable looks-same ([0173a7a](https://github.com/gemini-testing/hermione/commit/0173a7a))



<a name="1.2.0"></a>
# [1.2.0](https://github.com/gemini-testing/hermione/compare/v1.1.0...v1.2.0) (2018-12-26)


### Features

* pass diff bounds to error from looks-same ([fbb73c3](https://github.com/gemini-testing/hermione/commit/fbb73c3))



<a name="1.1.0"></a>
# [1.1.0](https://github.com/gemini-testing/hermione/compare/v1.0.3...v1.1.0) (2018-12-25)


### Features

* w3c browsers support ([49aa5dd](https://github.com/gemini-testing/hermione/commit/49aa5dd))



<a name="1.0.3"></a>
## [1.0.3](https://github.com/gemini-testing/hermione/compare/v1.0.2...v1.0.3) (2018-12-18)


### Bug Fixes

* collect correct statistics for tests run ([c0abd8d](https://github.com/gemini-testing/hermione/commit/c0abd8d))



<a name="1.0.2"></a>
## [1.0.2](https://github.com/gemini-testing/hermione/compare/v1.0.1...v1.0.2) (2018-12-14)



<a name="1.0.1"></a>
## [1.0.1](https://github.com/gemini-testing/hermione/compare/v1.0.0...v1.0.1) (2018-12-13)


### Bug Fixes

* do not convert ref image file to base64 to get size ([b1b8ef8](https://github.com/gemini-testing/hermione/commit/b1b8ef8))



<a name="1.0.0"></a>
# [1.0.0](https://github.com/gemini-testing/hermione/compare/v0.94.0...v1.0.0) (2018-11-29)


### Features

* add image sizes to "assertViewResults" ([e84ce6d](https://github.com/gemini-testing/hermione/commit/e84ce6d))


### BREAKING CHANGES

* now "assertViewResults" contains image path and size instead of only path



<a name="0.94.0"></a>
# [0.94.0](https://github.com/gemini-testing/hermione/compare/v0.93.0...v0.94.0) (2018-11-29)


### Features

* Ability to add test to current run ([#335](https://github.com/gemini-testing/hermione/issues/335)) ([33900b3](https://github.com/gemini-testing/hermione/commit/33900b3))



<a name="0.93.0"></a>
# [0.93.0](https://github.com/gemini-testing/hermione/compare/v0.92.0...v0.93.0) (2018-11-26)


### Features

* add 'pid' in which test is executed to meta info ([e530784](https://github.com/gemini-testing/hermione/commit/e530784))
* implement events interceptor API for plugins ([d8a4199](https://github.com/gemini-testing/hermione/commit/d8a4199))



<a name="0.92.0"></a>
# [0.92.0](https://github.com/gemini-testing/hermione/compare/v0.91.0...v0.92.0) (2018-11-08)


### Features

* expose errors from before hook and test fn ([#328](https://github.com/gemini-testing/hermione/issues/328)) ([2dbc1b3](https://github.com/gemini-testing/hermione/commit/2dbc1b3))



<a name="0.91.0"></a>
# [0.91.0](https://github.com/gemini-testing/hermione/compare/v0.90.2...v0.91.0) (2018-11-02)


### Bug Fixes

* do not restore windowSize after its change in test ([22d4ab3](https://github.com/gemini-testing/hermione/commit/22d4ab3))


### Features

* set window size from config before each test ([b4665cf](https://github.com/gemini-testing/hermione/commit/b4665cf))



<a name="0.90.2"></a>
## [0.90.2](https://github.com/gemini-testing/hermione/compare/v0.90.1...v0.90.2) (2018-10-27)


### Bug Fixes

* avoid hermioneCtx sharing between different test runs ([2917922](https://github.com/gemini-testing/hermione/commit/2917922))



<a name="0.90.1"></a>
## [0.90.1](https://github.com/gemini-testing/hermione/compare/v0.89.0...v0.90.1) (2018-10-02)


### Bug Fixes

* reset window size on default before the test is started ([8357206](https://github.com/gemini-testing/hermione/commit/8357206))


### Features

* add debug mode ([aaa42b7](https://github.com/gemini-testing/hermione/commit/aaa42b7))



<a name="0.90.0"></a>
# [0.90.0](https://github.com/gemini-testing/hermione/compare/v0.89.0...v0.90.0) (2018-09-17)


### Bug Fixes

* reset window size on default before the test is started ([8357206](https://github.com/gemini-testing/hermione/commit/8357206))


### Features

* add debug mode ([aaa42b7](https://github.com/gemini-testing/hermione/commit/aaa42b7))



<a name="0.89.1"></a>
## [0.89.1](https://github.com/gemini-testing/hermione/compare/v0.89.0...v0.89.1) (2018-09-14)


### Bug Fixes

* reset window size on default before the test is started ([8357206](https://github.com/gemini-testing/hermione/commit/8357206))



<a name="0.89.0"></a>
# [0.89.0](https://github.com/gemini-testing/hermione/compare/v0.87.0...v0.89.0) (2018-09-13)


### Features

* add option 'pageLoadTimeout' ([7cf389b](https://github.com/gemini-testing/hermione/commit/7cf389b))
* stub browser commands in broken session ([c61c927](https://github.com/gemini-testing/hermione/commit/c61c927))



<a name="0.88.0"></a>
# [0.88.0](https://github.com/gemini-testing/hermione/compare/v0.87.0...v0.88.0) (2018-09-13)


### Features

* stub browser commands in broken session ([c61c927](https://github.com/gemini-testing/hermione/commit/c61c927))



<a name="0.87.0"></a>
# [0.87.0](https://github.com/gemini-testing/hermione/compare/v0.85.0...v0.87.0) (2018-09-12)


### Bug Fixes

* set orientation before each test ([5dee565](https://github.com/gemini-testing/hermione/commit/5dee565))


### Features

* add "antialiasingTolerance" option ([88d1d1c](https://github.com/gemini-testing/hermione/commit/88d1d1c))



<a name="0.86.0"></a>
# [0.86.0](https://github.com/gemini-testing/hermione/compare/v0.85.0...v0.86.0) (2018-09-11)


### Features

* add "antialiasingTolerance" option ([88d1d1c](https://github.com/gemini-testing/hermione/commit/88d1d1c))



<a name="0.85.0"></a>
# [0.85.0](https://github.com/gemini-testing/hermione/compare/v0.84.0...v0.85.0) (2018-09-04)


### Features

* move mouse cursor to "body" coordinates 0,0 before each run test ([2c16f81](https://github.com/gemini-testing/hermione/commit/2c16f81))


### Reverts

* reset cursor position to (0, 0) before open the url ([4af3771](https://github.com/gemini-testing/hermione/commit/4af3771))



<a name="0.84.0"></a>
# [0.84.0](https://github.com/gemini-testing/hermione/compare/v0.82.0...v0.84.0) (2018-09-04)


### Features

* 'orientation' command waits for screen rotate ([2e23fe4](https://github.com/gemini-testing/hermione/commit/2e23fe4))
* add option 'resetCursor' ([0e6f767](https://github.com/gemini-testing/hermione/commit/0e6f767))
* reset cursor position to (0, 0) before open the url ([cab14ee](https://github.com/gemini-testing/hermione/commit/cab14ee))



<a name="0.83.0"></a>
# [0.83.0](https://github.com/gemini-testing/hermione/compare/v0.82.0...v0.83.0) (2018-08-28)


### Features

* reset cursor position to (0, 0) before open the url ([cab14ee](https://github.com/gemini-testing/hermione/commit/cab14ee))



<a name="0.82.0"></a>
# [0.82.0](https://github.com/gemini-testing/hermione/compare/v0.81.2...v0.82.0) (2018-08-19)


### Features

* run retries first ([82a08a7](https://github.com/gemini-testing/hermione/commit/82a08a7))



<a name="0.81.2"></a>
## [0.81.2](https://github.com/gemini-testing/hermione/compare/v0.81.1...v0.81.2) (2018-08-13)



<a name="0.81.1"></a>
## [0.81.1](https://github.com/gemini-testing/hermione/compare/v0.81.0...v0.81.1) (2018-08-09)



<a name="0.81.0"></a>
# [0.81.0](https://github.com/gemini-testing/hermione/compare/v0.79.2...v0.81.0) (2018-08-09)


### Bug Fixes

* free browser in worker test runner ([3d8d4fe](https://github.com/gemini-testing/hermione/commit/3d8d4fe))


### Features

* reset cursor position to (0, 0) before running test ([1af4309](https://github.com/gemini-testing/hermione/commit/1af4309))



<a name="0.80.0"></a>
# [0.80.0](https://github.com/gemini-testing/hermione/compare/v0.79.2...v0.80.0) (2018-08-08)


### Features

* reset cursor position to (0, 0) before running test ([1af4309](https://github.com/gemini-testing/hermione/commit/1af4309))



<a name="0.79.5"></a>
## [0.79.5](https://github.com/gemini-testing/hermione/compare/v0.79.2...v0.79.5) (2018-07-31)



<a name="0.79.4"></a>
## [0.79.4](https://github.com/gemini-testing/hermione/compare/v0.79.2...v0.79.4) (2018-07-27)



<a name="0.79.3"></a>
## [0.79.3](https://github.com/gemini-testing/hermione/compare/v0.79.2...v0.79.3) (2018-07-27)



<a name="0.79.2"></a>
## [0.79.2](https://github.com/gemini-testing/hermione/compare/v0.79.0...v0.79.2) (2018-07-27)


### Bug Fixes

* tests doesn't run ([1484bb9](https://github.com/gemini-testing/hermione/commit/1484bb9))


### Reverts

* reset cursor position to 0, 0 before running test ([33decf1](https://github.com/gemini-testing/hermione/commit/33decf1))



<a name="0.79.1"></a>
## [0.79.1](https://github.com/gemini-testing/hermione/compare/v0.79.0...v0.79.1) (2018-07-26)


### Reverts

* reset cursor position to 0, 0 before running test ([33decf1](https://github.com/gemini-testing/hermione/commit/33decf1))



<a name="0.79.0"></a>
# [0.79.0](https://github.com/gemini-testing/hermione/compare/v0.78.4...v0.79.0) (2018-07-25)


### Bug Fixes

* test.hermioneCtx not acceptable inside test callback ([c069f57](https://github.com/gemini-testing/hermione/commit/c069f57))


### Features

* remove backwards compatibility layer in TestCollection ([dfd9e72](https://github.com/gemini-testing/hermione/commit/dfd9e72))
* remove suite field in *_FILE_READ events ([91c0799](https://github.com/gemini-testing/hermione/commit/91c0799))
* reset cursor position to 0, 0 before running test ([45a11e7](https://github.com/gemini-testing/hermione/commit/45a11e7))
* set default browser orientation before each test ([990a210](https://github.com/gemini-testing/hermione/commit/990a210))



<a name="0.78.4"></a>
## [0.78.4](https://github.com/gemini-testing/hermione/compare/v0.78.3...v0.78.4) (2018-07-19)


### Bug Fixes

* hermione.skip skips always for one browser ([8c6de4b](https://github.com/gemini-testing/hermione/commit/8c6de4b))



<a name="0.78.3"></a>
## [0.78.3](https://github.com/gemini-testing/hermione/compare/v0.78.2...v0.78.3) (2018-07-19)


### Bug Fixes

* .only does not work for all browsers ([fb855ca](https://github.com/gemini-testing/hermione/commit/fb855ca))



<a name="0.78.2"></a>
## [0.78.2](https://github.com/gemini-testing/hermione/compare/v0.78.1...v0.78.2) (2018-07-18)


### Bug Fixes

* hooks does not have browserId property ([75c7d53](https://github.com/gemini-testing/hermione/commit/75c7d53))



<a name="0.78.1"></a>
## [0.78.1](https://github.com/gemini-testing/hermione/compare/v0.78.0...v0.78.1) (2018-07-17)


### Bug Fixes

* tests do not fail on assert view fails ([1a5ed83](https://github.com/gemini-testing/hermione/commit/1a5ed83))



<a name="0.78.0"></a>
# [0.78.0](https://github.com/gemini-testing/hermione/compare/v0.77.0...v0.78.0) (2018-07-15)


### Features

* use own runner instead of mocha in workers ([dad7707](https://github.com/gemini-testing/hermione/commit/dad7707))



<a name="0.77.0"></a>
# [0.77.0](https://github.com/gemini-testing/hermione/compare/v0.76.1...v0.77.0) (2018-07-06)


### Features

* silently skip disabled tests ([e0c37eb](https://github.com/gemini-testing/hermione/commit/e0c37eb))



<a name="0.76.1"></a>
## [0.76.1](https://github.com/gemini-testing/hermione/compare/v0.76.0...v0.76.1) (2018-07-04)


### Bug Fixes

* extend runnables api on parser events ([85dbc7b](https://github.com/gemini-testing/hermione/commit/85dbc7b))



<a name="0.76.0"></a>
# [0.76.0](https://github.com/gemini-testing/hermione/compare/v0.75.0...v0.76.0) (2018-07-02)


### Features

* ability to add test controllers on BEFORE_FILE_READ ([1c5082e](https://github.com/gemini-testing/hermione/commit/1c5082e))



<a name="0.75.0"></a>
# [0.75.0](https://github.com/gemini-testing/hermione/compare/v0.74.0...v0.75.0) (2018-06-29)


### Features

* add 'screenshotDelay' option ([ced8e9f](https://github.com/gemini-testing/hermione/commit/ced8e9f))



<a name="0.74.0"></a>
# [0.74.0](https://github.com/gemini-testing/hermione/compare/v0.73.0...v0.74.0) (2018-06-26)


### Features

* ability to iterate over all root suites in test collection ([bc02934](https://github.com/gemini-testing/hermione/commit/bc02934))



<a name="0.73.0"></a>
# [0.73.0](https://github.com/gemini-testing/hermione/compare/v0.72.0...v0.73.0) (2018-06-26)


### Bug Fixes

* TestCollection: do not add empty browser to properties ([63bdc77](https://github.com/gemini-testing/hermione/commit/63bdc77))


### Features

* AFTER_TESTS_READ event ([45c4acb](https://github.com/gemini-testing/hermione/commit/45c4acb))



<a name="0.72.0"></a>
# [0.72.0](https://github.com/gemini-testing/hermione/compare/v0.71.0...v0.72.0) (2018-06-25)


### Bug Fixes

* add backwards compatibility for hermione.readTests ([c19235f](https://github.com/gemini-testing/hermione/commit/c19235f))
* passthrough "pixelRatio" to image comparator ([6775838](https://github.com/gemini-testing/hermione/commit/6775838))


### Features

* ability to enable/disable tests in TestCollection ([cac56f7](https://github.com/gemini-testing/hermione/commit/cac56f7))
* ability to pass TestCollection to run method ([6e8582b](https://github.com/gemini-testing/hermione/commit/6e8582b))
* own test runner instead of mocha for master process ([667ca48](https://github.com/gemini-testing/hermione/commit/667ca48))
* parse tests before runner start ([67a5ac7](https://github.com/gemini-testing/hermione/commit/67a5ac7))
* SuiteCollection.eachTest method ([0871b7d](https://github.com/gemini-testing/hermione/commit/0871b7d))



<a name="0.71.0"></a>
# [0.71.0](https://github.com/gemini-testing/hermione/compare/v0.70.0...v0.71.0) (2018-06-08)


### Features

* do not retry test failed with no ref image error ([2055f4e](https://github.com/gemini-testing/hermione/commit/2055f4e))



<a name="0.70.0"></a>
# [0.70.0](https://github.com/gemini-testing/hermione/compare/v0.68.0...v0.70.0) (2018-06-04)


### Bug Fixes

* handle cases when error does not have 'hermioneCtx' ([5a82074](https://github.com/gemini-testing/hermione/commit/5a82074))


### Features

* add ability to exlude paths in 'readTests' ([724c7b4](https://github.com/gemini-testing/hermione/commit/724c7b4))



<a name="0.69.0"></a>
# [0.69.0](https://github.com/gemini-testing/hermione/compare/v0.68.0...v0.69.0) (2018-05-17)


### Features

* add ability to exlude paths in 'readTests' ([724c7b4](https://github.com/gemini-testing/hermione/commit/724c7b4))



<a name="0.68.0"></a>
# [0.68.0](https://github.com/gemini-testing/hermione/compare/v0.67.0...v0.68.0) (2018-05-17)


### Features

* do not fail on first 'assertView' error ([3bd61d4](https://github.com/gemini-testing/hermione/commit/3bd61d4))



<a name="0.67.0"></a>
# [0.67.0](https://github.com/gemini-testing/hermione/compare/v0.66.1...v0.67.0) (2018-05-07)


### Features

* introduce hermione.halt method ([ac028fe](https://github.com/gemini-testing/hermione/commit/ac028fe))



<a name="0.66.1"></a>
## [0.66.1](https://github.com/gemini-testing/hermione/compare/v0.66.0...v0.66.1) (2018-04-26)


### Bug Fixes

* config property "shouldRetry" now works correctly ([2645612](https://github.com/gemini-testing/hermione/commit/2645612))



<a name="0.66.0"></a>
# [0.66.0](https://github.com/gemini-testing/hermione/compare/v0.65.2...v0.66.0) (2018-04-10)


### Features

* return all meta on getMeta call without arguments ([79264e2](https://github.com/gemini-testing/hermione/commit/79264e2))



<a name="0.65.2"></a>
## [0.65.2](https://github.com/gemini-testing/hermione/compare/v0.65.1...v0.65.2) (2018-03-19)



<a name="0.65.1"></a>
## [0.65.1](https://github.com/gemini-testing/hermione/compare/v0.65.0...v0.65.1) (2018-03-16)


### Bug Fixes

* sync config in worker before running tests ([ba68fea](https://github.com/gemini-testing/hermione/commit/ba68fea))



<a name="0.65.0"></a>
# [0.65.0](https://github.com/gemini-testing/hermione/compare/v0.64.0...v0.65.0) (2018-03-15)


### Features

* add 'hermioneCtx' field to the test after reading the file ([f94c91c](https://github.com/gemini-testing/hermione/commit/f94c91c))
* emit 'INIT' event for each worker ([f9f7f54](https://github.com/gemini-testing/hermione/commit/f9f7f54))



<a name="0.64.0"></a>
# [0.64.0](https://github.com/gemini-testing/hermione/compare/v0.63.0...v0.64.0) (2018-03-15)


### Features

* add 'ignoreElements' options to 'assertView' command ([bd10710](https://github.com/gemini-testing/hermione/commit/bd10710))
* option 'compositeImage' for 'assertView' command ([610df5e](https://github.com/gemini-testing/hermione/commit/610df5e))
* option 'screenshotMode' ([35dd71e](https://github.com/gemini-testing/hermione/commit/35dd71e))
* wrap tests running in command ([fcbd8bf](https://github.com/gemini-testing/hermione/commit/fcbd8bf))



<a name="0.63.0"></a>
# [0.63.0](https://github.com/gemini-testing/hermione/compare/v0.62.0...v0.63.0) (2018-03-02)


### Bug Fixes

* optional timeouts by default does not equal to httpTimeout ([aa670d9](https://github.com/gemini-testing/hermione/commit/aa670d9))


### Features

* assert view by selectors ([b090a5f](https://github.com/gemini-testing/hermione/commit/b090a5f))
* do not use webdriverio screenshotOnReject option ([326a8d0](https://github.com/gemini-testing/hermione/commit/326a8d0))
* drop node versions previous to 8 ([5136865](https://github.com/gemini-testing/hermione/commit/5136865))
* take screenshot on test or hook fail ([ec47808](https://github.com/gemini-testing/hermione/commit/ec47808))



<a name="0.62.0"></a>
# [0.62.0](https://github.com/gemini-testing/hermione/compare/v0.61.0...v0.62.0) (2018-02-20)


### Features

* add screenshotOnReject and screenshotOnRejectTimeout options ([236efaf](https://github.com/gemini-testing/hermione/commit/236efaf))



<a name="0.61.0"></a>
# [0.61.0](https://github.com/gemini-testing/hermione/compare/v0.60.0...v0.61.0) (2018-02-14)


### Features

* introduce shouldRerty config option ([pull/224](https://github.com/gemini-testing/hermione/pull/224))

<a name="0.60.1"></a>
## [0.60.1](https://github.com/gemini-testing/hermione/compare/v0.60.0...v0.60.1) (2018-02-09)


### Bug Fixes

* do not store all mocha instances in workers ([ed7aab4](https://github.com/gemini-testing/hermione/commit/ed7aab4))
* drop webdriverio command history after each test in workers ([51c4daf](https://github.com/gemini-testing/hermione/commit/51c4daf))



<a name="0.60.0"></a>
# [0.60.0](https://github.com/gemini-testing/hermione/compare/v0.59.0...v0.60.0) (2018-02-08)


### Features

* ability to restart workers after some number of tests ([4a42b0d](https://github.com/gemini-testing/hermione/commit/4a42b0d))



<a name="0.59.0"></a>
# [0.59.0](https://github.com/gemini-testing/hermione/compare/v0.58.1...v0.59.0) (2018-02-08)


### Features

* ability to restart workers on crash ([e7e08c2](https://github.com/gemini-testing/hermione/commit/e7e08c2))



<a name="0.58.1"></a>
## [0.58.1](https://github.com/gemini-testing/hermione/compare/v0.58.0...v0.58.1) (2018-02-07)


### Bug Fixes

* browser calibration ([2391a28](https://github.com/gemini-testing/hermione/commit/2391a28))
* do not retry worker init on fail ([28352cd](https://github.com/gemini-testing/hermione/commit/28352cd))



<a name="0.58.0"></a>
# [0.58.0](https://github.com/gemini-testing/hermione/compare/v0.57.0...v0.58.0) (2018-02-04)


### Features

* **stats:** emit test statistics on RUNNER_END ([320da47](https://github.com/gemini-testing/hermione/commit/320da47))



<a name="0.57.0"></a>
# [0.57.0](https://github.com/gemini-testing/hermione/compare/v0.56.2...v0.57.0) (2018-02-04)


### Bug Fixes

* init temp in master process ([5dd0dee](https://github.com/gemini-testing/hermione/commit/5dd0dee))


### Features

* option '--update-refs' for 'assertView' command ([186ca73](https://github.com/gemini-testing/hermione/commit/186ca73))



<a name="0.56.2"></a>
## [0.56.2](https://github.com/gemini-testing/hermione/compare/v0.56.1...v0.56.2) (2018-01-30)


### Bug Fixes

* init save diff function in master process ([c263d87](https://github.com/gemini-testing/hermione/commit/c263d87))



<a name="0.56.1"></a>
## [0.56.1](https://github.com/gemini-testing/hermione/compare/v0.56.0...v0.56.1) (2018-01-27)


### Bug Fixes

* afterEach hook error overwrites original test error ([d29f549](https://github.com/gemini-testing/hermione/commit/d29f549))



<a name="0.56.0"></a>
# [0.56.0](https://github.com/gemini-testing/hermione/compare/v0.55.0...v0.56.0) (2018-01-17)


### Bug Fixes

* do not overwrite system.mochaOpts.grep property in workers ([8dce8ad](https://github.com/gemini-testing/hermione/commit/8dce8ad))


### Features

* use new glob-extra version ([2e7509f](https://github.com/gemini-testing/hermione/commit/2e7509f))



<a name="0.55.0"></a>
# [0.55.0](https://github.com/gemini-testing/hermione/compare/v0.54.3...v0.55.0) (2018-01-12)


### Bug Fixes

* update webdriverio fork to 4.9.11 ([2f0b1fc](https://github.com/gemini-testing/hermione/commit/2f0b1fc))


### Features

* add ability to calibrate image before capturing ([c80f6f0](https://github.com/gemini-testing/hermione/commit/c80f6f0))
* add assertView command ([49427cc](https://github.com/gemini-testing/hermione/commit/49427cc))



<a name="0.54.3"></a>
## [0.54.3](https://github.com/gemini-testing/hermione/compare/v0.54.2...v0.54.3) (2017-12-08)


### Bug Fixes

* set id method even for skipped suites by mocha ([ce7bc89](https://github.com/gemini-testing/hermione/commit/ce7bc89))



<a name="0.54.2"></a>
## [0.54.2](https://github.com/gemini-testing/hermione/compare/v0.54.1...v0.54.2) (2017-12-07)


### Bug Fixes

* stop emitting suite end after each test ([e78eed7](https://github.com/gemini-testing/hermione/commit/e78eed7))



<a name="0.54.1"></a>
## [0.54.1](https://github.com/gemini-testing/hermione/compare/v0.54.0...v0.54.1) (2017-12-07)


### Bug Fixes

* allow unknown options before parsing config file ([b79ad34](https://github.com/gemini-testing/hermione/commit/b79ad34))



<a name="0.54.0"></a>
# [0.54.0](https://github.com/gemini-testing/hermione/compare/v0.53.0...v0.54.0) (2017-12-07)


### Features

* allow to extend cli parser via CLI event ([6d5f96a](https://github.com/gemini-testing/hermione/commit/6d5f96a))



<a name="0.53.0"></a>
# [0.53.0](https://github.com/gemini-testing/hermione/compare/v0.52.1...v0.53.0) (2017-12-01)


### Features

* load plugins synchronously in constructor, add async INIT event ([128681a](https://github.com/gemini-testing/hermione/commit/128681a))



<a name="0.52.1"></a>
## [0.52.1](https://github.com/gemini-testing/hermione/compare/v0.52.0...v0.52.1) (2017-11-22)



<a name="0.52.0"></a>
# [0.52.0](https://github.com/gemini-testing/hermione/compare/v0.51.0...v0.52.0) (2017-11-10)


### Features

* add hermione.init method ([#196](https://github.com/gemini-testing/hermione/issues/196)) ([d532886](https://github.com/gemini-testing/hermione/commit/d532886))



<a name="0.51.0"></a>
# [0.51.0](https://github.com/gemini-testing/hermione/compare/v0.50.3...v0.51.0) (2017-11-01)


### Features

* wait for plugins load ([6499b2c](https://github.com/gemini-testing/hermione/commit/6499b2c))



<a name="0.50.3"></a>
## [0.50.3](https://github.com/gemini-testing/hermione/compare/v0.50.2...v0.50.3) (2017-10-31)



<a name="0.50.2"></a>
## [0.50.2](https://github.com/gemini-testing/hermione/compare/v0.50.1...v0.50.2) (2017-10-19)


### Bug Fixes

* **mocha-adapter:** restore browser at each mocha reinitialization ([44bc801](https://github.com/gemini-testing/hermione/commit/44bc801))
* **proxy-reporter:** rewrite on ES6 ([69ffefe](https://github.com/gemini-testing/hermione/commit/69ffefe))



<a name="0.50.1"></a>
## [0.50.1](https://github.com/gemini-testing/hermione/compare/v0.50.0...v0.50.1) (2017-10-19)



<a name="0.50.0"></a>
# [0.50.0](https://github.com/gemini-testing/hermione/compare/v0.46.0...v0.50.0) (2017-10-17)


### Bug Fixes

* Fix session rejection logic ([6393c6e](https://github.com/gemini-testing/hermione/commit/6393c6e))


<a name="0.49.0"></a>
# [0.49.0](https://github.com/gemini-testing/hermione/compare/v0.48.1...v0.49.0) (2017-10-05)


### Features

* add common data transfer between main process and subprocess ([88011c4](https://github.com/gemini-testing/hermione/commit/88011c4))



<a name="0.48.1"></a>
## [0.48.1](https://github.com/gemini-testing/hermione/compare/v0.48.0...v0.48.1) (2017-09-29)


### Bug Fixes

* update webdriver.io fork with keep-alive fix ([8926d5d](https://github.com/gemini-testing/hermione/commit/8926d5d))



<a name="0.48.0"></a>
# [0.48.0](https://github.com/gemini-testing/hermione/compare/v0.47.0...v0.48.0) (2017-09-20)


### Features

* add windowSize option ([a71ea86](https://github.com/gemini-testing/hermione/commit/a71ea86))



<a name="0.47.0"></a>
# [0.47.0](https://github.com/gemini-testing/hermione/compare/v0.46.0...v0.47.0) (2017-09-19)


### Features

* add method 'isWorker' to the API ([0698611](https://github.com/gemini-testing/hermione/commit/0698611))



<a name="0.46.0"></a>
# [0.46.0](https://github.com/gemini-testing/hermione/compare/v0.45.1...v0.46.0) (2017-09-15)


### Features

* forbid using of 'before' and 'after' hooks in tests ([0d76164](https://github.com/gemini-testing/hermione/commit/0d76164))



<a name="0.45.1"></a>
## [0.45.1](https://github.com/gemini-testing/hermione/compare/v0.45.0...v0.45.1) (2017-09-13)


### Bug Fixes

* update package-lock.json ([7e7dee0](https://github.com/gemini-testing/hermione/commit/7e7dee0))



<a name="0.45.0"></a>
# [0.45.0](https://github.com/gemini-testing/hermione/compare/v0.44.0...v0.45.0) (2017-09-13)


### Bug Fixes

* fix up opera in webdriverio fork ([5f49845](https://github.com/gemini-testing/hermione/commit/5f49845))


### Features

* **node-support:** drop of support node below 6.4.0 ([dae8e6c](https://github.com/gemini-testing/hermione/commit/dae8e6c))


### BREAKING CHANGES

* **node-support:** support only node>=6.4.0



<a name="0.44.0"></a>
# [0.44.0](https://github.com/gemini-testing/hermione/compare/v0.37.4...v0.44.0) (2017-09-10)


### Features

* extend test error with original selenium error ([500d30c](https://github.com/gemini-testing/hermione/commit/500d30c))



<a name="0.43.8"></a>
## [0.43.8](https://github.com/gemini-testing/hermione/compare/v0.43.7...v0.43.8) (2017-09-08)


### Bug Fixes

* running of tests with option 'grep' fails with exception ([4c80583](https://github.com/gemini-testing/hermione/commit/4c80583))



<a name="0.43.7"></a>
## [0.43.7](https://github.com/gemini-testing/hermione/compare/v0.43.6...v0.43.7) (2017-08-29)


### Bug Fixes

* do not hang on errors in config.prepareBrowser ([643a344](https://github.com/gemini-testing/hermione/commit/643a344))



<a name="0.43.6"></a>
## [0.43.6](https://github.com/gemini-testing/hermione/compare/v0.43.5...v0.43.6) (2017-08-25)


### Bug Fixes

* specify the release branch of forked 'worker-farm' ([649cec6](https://github.com/gemini-testing/hermione/commit/649cec6))



<a name="0.43.5"></a>
## [0.43.5](https://github.com/gemini-testing/hermione/compare/v0.43.4...v0.43.5) (2017-08-18)


### Bug Fixes

* correct passing of errors from subprocesses to the main process ([13e4c17](https://github.com/gemini-testing/hermione/commit/13e4c17))



<a name="0.43.4"></a>
## [0.43.4](https://github.com/gemini-testing/hermione/compare/v0.43.3...v0.43.4) (2017-08-17)


### Bug Fixes

* pass meta info from workers to the main process ([0e8580a](https://github.com/gemini-testing/hermione/commit/0e8580a))



<a name="0.43.3"></a>
## [0.43.3](https://github.com/gemini-testing/hermione/compare/v0.43.2...v0.43.3) (2017-08-16)


### Bug Fixes

* do not restore existing 'global.hermione' variable ([e046226](https://github.com/gemini-testing/hermione/commit/e046226))



<a name="0.43.2"></a>
## [0.43.2](https://github.com/gemini-testing/hermione/compare/v0.43.1...v0.43.2) (2017-08-15)


### Bug Fixes

* correct passing of 'screenshotOnReject' option in subprocesses ([8faae64](https://github.com/gemini-testing/hermione/commit/8faae64))



<a name="0.43.1"></a>
## [0.43.1](https://github.com/gemini-testing/hermione/compare/v0.43.0...v0.43.1) (2017-08-15)


### Bug Fixes

* do not start browsers for skipped suites ([c3d6bb1](https://github.com/gemini-testing/hermione/commit/c3d6bb1))



<a name="0.43.0"></a>
# [0.43.0](https://github.com/gemini-testing/hermione/compare/v0.42.0...v0.43.0) (2017-08-15)


### Features

* running of tests in subprocesses ([fbb51f6](https://github.com/gemini-testing/hermione/commit/fbb51f6))



<a name="0.42.0"></a>
# [0.42.0](https://github.com/gemini-testing/hermione/compare/v0.41.0...v0.42.0) (2017-08-08)


### Features

* extend browser config with its id ([06e85f6](https://github.com/gemini-testing/hermione/commit/06e85f6))
* NEW_BROWSER event ([480401a](https://github.com/gemini-testing/hermione/commit/480401a))



<a name="0.41.0"></a>
# [0.41.0](https://github.com/gemini-testing/hermione/compare/v0.40.0...v0.41.0) (2017-08-01)


### Features

* update lodash version to 4.x ([68500a0](https://github.com/gemini-testing/hermione/commit/68500a0))



<a name="0.40.0"></a>
# [0.40.0](https://github.com/gemini-testing/hermione/compare/v0.39.1...v0.40.0) (2017-08-01)


### Features

* add method 'isFailed' to the API ([5852b13](https://github.com/gemini-testing/hermione/commit/5852b13))
* add options 'loadPlugins' to the API method 'readTests' ([7a68f0a](https://github.com/gemini-testing/hermione/commit/7a68f0a))



<a name="0.39.1"></a>
## [0.39.1](https://github.com/gemini-testing/hermione/compare/v0.39.0...v0.39.1) (2017-07-25)


### Bug Fixes

* load plugins early ([5c00a24](https://github.com/gemini-testing/hermione/commit/5c00a24))



<a name="0.39.0"></a>
# [0.39.0](https://github.com/gemini-testing/hermione/compare/v0.37.4...v0.39.0) (2017-07-04)


### Features

* provide the ability to modify retries count from plugins ([fc1a372](https://github.com/gemini-testing/hermione/commit/fc1a372))



<a name="0.38.0"></a>
# [0.38.0](https://github.com/gemini-testing/hermione/compare/v0.21.0...v0.38.0) (2017-07-02)


### Features

* reject session if error matches on patterns from config ([775e0ea](https://github.com/gemini-testing/hermione/commit/775e0ea))



<a name="0.37.4"></a>
## [0.37.4](https://github.com/gemini-testing/hermione/compare/v0.37.3...v0.37.4) (2017-06-23)


### Bug Fixes

* 'hermione.only.in' functionality ([6f575c8](https://github.com/gemini-testing/hermione/commit/6f575c8))



<a name="0.37.3"></a>
## [0.37.3](https://github.com/gemini-testing/hermione/compare/v0.37.2...v0.37.3) (2017-06-20)


### Bug Fixes

* ignore memory leaks warnings for mocha suites ([93ed298](https://github.com/gemini-testing/hermione/commit/93ed298))



<a name="0.37.2"></a>
## [0.37.2](https://github.com/gemini-testing/hermione/compare/v0.37.1...v0.37.2) (2017-06-19)


### Bug Fixes

* Replace mocha timeouts with promise timeouts ([9d648d9](https://github.com/gemini-testing/hermione/commit/9d648d9))



<a name="0.37.1"></a>
## [0.37.1](https://github.com/gemini-testing/hermione/compare/v0.37.0...v0.37.1) (2017-06-14)


### Bug Fixes

* do not run 'before' and 'after' hooks for a skipped suite ([2da0467](https://github.com/gemini-testing/hermione/commit/2da0467))



<a name="0.37.0"></a>
# [0.37.0](https://github.com/gemini-testing/hermione/compare/v0.36.0...v0.37.0) (2017-06-08)


### Major

* `before` hook is similar in meaning to `beforeEach` one while running tests

### Features

* implement 'testsPerSession' option ([a5f817e](https://github.com/gemini-testing/hermione/commit/a5f817e))



<a name="0.36.0"></a>
# [0.36.0](https://github.com/gemini-testing/hermione/compare/v0.35.1...v0.36.0) (2017-05-04)


### Bug Fixes

* do not pass browser to retried tests ([b2cb7cc](https://github.com/gemini-testing/hermione/commit/b2cb7cc))


### Features

* emit BEGIN event between runners initialize and tests execution ([6e3f56b](https://github.com/gemini-testing/hermione/commit/6e3f56b))



<a name="0.35.1"></a>
## [0.35.1](https://github.com/gemini-testing/hermione/compare/v0.35.0...v0.35.1) (2017-05-02)


### Bug Fixes

* handle 'before*' hooks failure correctly ([a0934ba](https://github.com/gemini-testing/hermione/commit/a0934ba))



<a name="0.35.0"></a>
# [0.35.0](https://github.com/gemini-testing/hermione/compare/v0.34.0...v0.35.0) (2017-04-25)


### Features

* remove handling of 'before*'-hooks failure in tests ([0c74de2](https://github.com/gemini-testing/hermione/commit/0c74de2))
* improve the algorithm of retries ([b2d91b7](https://github.com/gemini-testing/hermione/commit/b2d91b7))



<a name="0.34.0"></a>
# [0.34.0](https://github.com/gemini-testing/hermione/compare/v0.33.0...v0.34.0) (2017-04-22)


### Bug Fixes

* add correct error handling in before and beforeEach hooks ([561342a](https://github.com/gemini-testing/hermione/commit/561342a))



<a name="0.33.0"></a>
# [0.33.0](https://github.com/gemini-testing/hermione/compare/v0.31.0...v0.33.0) (2017-04-05)


### Features

* Add optional "meta" field for browser config ([3a80d66](https://github.com/gemini-testing/hermione/commit/3a80d66))
* add plain reporter ([3d30df9](https://github.com/gemini-testing/hermione/commit/3d30df9))



<a name="0.32.0"></a>
# [0.32.0](https://github.com/gemini-testing/hermione/compare/v0.21.0...v0.32.0) (2017-04-04)


### Features

* add plain reporter ([3d30df9](https://github.com/gemini-testing/hermione/commit/3d30df9))



<a name="0.31.0"></a>
# [0.31.0](https://github.com/gemini-testing/hermione/compare/v0.30.2...v0.31.0) (2017-04-03)


### Features

* make browser.url work like url.resolve ([727f78d](https://github.com/gemini-testing/hermione/commit/727f78d))



<a name="0.30.2"></a>
## [0.30.2](https://github.com/gemini-testing/hermione/compare/v0.30.1...v0.30.2) (2017-03-15)


### Bug Fixes

* ignore failed tests from mocha ([bd41074](https://github.com/gemini-testing/hermione/commit/bd41074))



<a name="0.30.1"></a>
## [0.30.1](https://github.com/gemini-testing/hermione/compare/v0.30.0...v0.30.1) (2017-03-15)


### Bug Fixes

* fail instead of hang on throws from event handlers ([6c1706a](https://github.com/gemini-testing/hermione/commit/6c1706a))



<a name="0.30.0"></a>
# [0.30.0](https://github.com/gemini-testing/hermione/compare/v0.28.4...v0.30.0) (2017-03-15)


### Features

* load plugins and pass events when reading files ([b402217](https://github.com/gemini-testing/hermione/commit/b402217))
* pass mocha suite on 'beforeFileRead' and 'afterFileRead' events ([3e25894](https://github.com/gemini-testing/hermione/commit/3e25894))



<a name="0.29.0"></a>
# [0.29.0](https://github.com/gemini-testing/hermione/compare/v0.21.0...v0.29.0) (2017-03-06)


### Features

* load plugins and pass events when reading files ([b402217](https://github.com/gemini-testing/hermione/commit/b402217))


<a name="0.28.4"></a>
## [0.28.4](https://github.com/gemini-testing/hermione/compare/v0.28.3...v0.28.4) (2017-03-02)


### Bug Fixes

* bug with file path on 'before all' hook ([a3ffee7](https://github.com/gemini-testing/hermione/commit/a3ffee7))



<a name="0.28.3"></a>
## [0.28.3](https://github.com/gemini-testing/hermione/compare/v0.28.2...v0.28.3) (2017-02-28)


### Bug Fixes

* the output to file path on 'before all' hook ([1378e75](https://github.com/gemini-testing/hermione/commit/1378e75))



<a name="0.28.2"></a>
## [0.28.2](https://github.com/gemini-testing/hermione/compare/v0.28.1...v0.28.2) (2017-02-23)


### Bug Fixes

* Do not save whole runnable object - decrease memory leaks ([d1c0224](https://github.com/gemini-testing/hermione/commit/d1c0224))



<a name="0.28.1"></a>
## [0.28.1](https://github.com/gemini-testing/hermione/compare/v0.28.0...v0.28.1) (2017-02-22)


### Bug Fixes

* Boolean env and cli vars reading ([fb5e932](https://github.com/gemini-testing/hermione/commit/fb5e932))



<a name="0.28.0"></a>
# [0.28.0](https://github.com/gemini-testing/hermione/compare/v0.27.0...v0.28.0) (2017-02-13)


### Features

* BEFORE_FILE_READ and AFTER_FILE_READ events ([f2a5593](https://github.com/gemini-testing/hermione/commit/f2a5593))



<a name="0.27.0"></a>
# [0.27.0](https://github.com/gemini-testing/hermione/compare/v0.25.1...v0.27.0) (2017-02-13)


### Bug Fixes

* Make sync and async events pass through separately ([87722ba](https://github.com/gemini-testing/hermione/commit/87722ba))


### Features

* Add hermione.only.notIn() helper ([17b4453](https://github.com/gemini-testing/hermione/commit/17b4453))



<a name="0.26.0"></a>
## [0.26.0](https://github.com/gemini-testing/hermione/compare/v0.25.2...v0.26.0) (2017-02-08)

### Features

* add helper hermione.only.notIn ([17b4453](https://github.com/gemini-testing/hermione/commit/17b4453))


<a name="0.25.2"></a>
## [0.25.2](https://github.com/gemini-testing/hermione/compare/v0.25.1...v0.25.2) (2017-02-07)


### Bug Fixes

* skip.only should skip only one test/suite below the record ([c13adc8](https://github.com/gemini-testing/hermione/commit/c13adc8))



<a name="0.25.1"></a>
## [0.25.1](https://github.com/gemini-testing/hermione/compare/v0.25.0...v0.25.1) (2017-01-25)


### Bug Fixes

* 'global.hermione' is not defined when reading tests via 'readTests' ([64ff66a](https://github.com/gemini-testing/hermione/commit/64ff66a))



<a name="0.25.0"></a>
# [0.25.0](https://github.com/gemini-testing/hermione/compare/v0.22.0...v0.25.0) (2017-01-25)


### Bug Fixes

* 'hermione.ctx' is not available in a callback of test ([a6fec7c](https://github.com/gemini-testing/hermione/commit/a6fec7c))
* Fix url decoration for urls without pathnames ([5df188e](https://github.com/gemini-testing/hermione/commit/5df188e))
* set meta info on before each hook ([f0ea113](https://github.com/gemini-testing/hermione/commit/f0ea113))


### Features

* add method 'hermione.ctx' to tests API ([0506da6](https://github.com/gemini-testing/hermione/commit/0506da6))



<a name="0.24.1"></a>
## [0.24.1](https://github.com/gemini-testing/hermione/compare/v0.24.0...v0.24.1) (2017-01-25)


### Bug Fixes

* 'hermione.ctx' is not available in a callback of test ([a6fec7c](https://github.com/gemini-testing/hermione/commit/a6fec7c))



<a name="0.24.0"></a>
# [0.24.0](https://github.com/gemini-testing/hermione/compare/v0.23.1...v0.24.0) (2017-01-25)


### Features

* add method 'hermione.ctx' to tests API ([0506da6](https://github.com/gemini-testing/hermione/commit/0506da6))



<a name="0.23.1"></a>
## [0.23.1](https://github.com/gemini-testing/hermione/compare/v0.23.0...v0.23.1) (2017-01-15)



<a name="0.23.0"></a>
# [0.23.0](https://github.com/gemini-testing/hermione/compare/v0.20.0...v0.23.0) (2016-12-30)


### Bug Fixes

* set meta info on before each hook ([f0ea113](https://github.com/gemini-testing/hermione/commit/f0ea113))


### Features

* add ability to specify sets in config ([b713732](https://github.com/gemini-testing/hermione/commit/b713732))
* make hermione instance available from hermione plugins ([0767d5f](https://github.com/gemini-testing/hermione/commit/0767d5f))
* remove hermione facade module ([738796b](https://github.com/gemini-testing/hermione/commit/738796b))



<a name="0.22.0"></a>
# [0.22.0](https://github.com/gemini-testing/hermione/compare/v0.15.3...v0.22.0) (2016-12-26)


### Bug Fixes

* correct resolving of baseUrl in config ([c010dc6](https://github.com/gemini-testing/hermione/commit/c010dc6))


### Features

* add ability to specify sets in config ([b713732](https://github.com/gemini-testing/hermione/commit/b713732))
* add option 'httpTimeout' ([8b747e0](https://github.com/gemini-testing/hermione/commit/8b747e0))
* add option 'sessionQuitTimeout' ([acc93f6](https://github.com/gemini-testing/hermione/commit/acc93f6))
* add option 'sessionRequestTimeout' ([a15b022](https://github.com/gemini-testing/hermione/commit/a15b022))
* add programmatic API ([248caf6](https://github.com/gemini-testing/hermione/commit/248caf6))
* make hermione instance available from hermione plugins ([0767d5f](https://github.com/gemini-testing/hermione/commit/0767d5f))
* remove hermione facade module ([738796b](https://github.com/gemini-testing/hermione/commit/738796b))



<a name="0.21.0"></a>
# [0.21.0](https://github.com/gemini-testing/hermione/compare/v0.20.0...v0.21.0) (2016-12-22)


### Features

* add ability to specify sets in config ([b713732](https://github.com/gemini-testing/hermione/commit/b713732))



<a name="0.20.0"></a>
# [0.20.0](https://github.com/gemini-testing/hermione/compare/v0.19.0...v0.20.0) (2016-12-20)


### Bug Fixes

* correct resolving of baseUrl in config ([c010dc6](https://github.com/gemini-testing/hermione/commit/c010dc6))


### Features

* add option 'sessionRequestTimeout' ([a15b022](https://github.com/gemini-testing/hermione/commit/a15b022))



# Changelog

## 0.19.0 - 2016-12-10

* feat: add API for tests reading

## 0.18.2 - 2016-12-05

* fix: `screenshotOnReject` may not be declared in config file

## 0.18.1 - 2016-12-02

* feat: add ability to configure timeout for take screenshot

## 0.18.0 - 2016-11-29

* major: Remove option `screenshotOnReject`
* feat: add option [sessionQuitTimeout](https://github.com/gemini-testing/hermione/blob/v0.18.0/README.md#sessionquittimeout)
* fix: more informative error if parsing of a config fails

## 0.17.0 - 2016-11-23

* Add programmatic API. See [doc](https://github.com/gemini-testing/hermione/blob/master/README.md#programmatic-api) for more details.

## 0.16.0 - 2016-11-17

* Add ability to run specific tests only in specific browsers without marking test as skipped in other browsers. See method [only](https://github.com/gemini-testing/hermione#only)
* Add ability to specify http timeout for requests to Selenium server

## 0.15.4 - 2016-11-16

* Fix: ability to override browser options from config

## 0.15.3 – 2016-11-11

* Added passing of browser identifier to `SESSION_START` and `SESSION_END` event handlers
* Added eslint code validation tool instead of jshint and jscs

## 0.15.2 – 2016-10-31

* Fixed bug with hermione freezing because of errors in `prepareBrowser` option in config

## 0.15.1 - 2016-10-26

* Added passing of runner instance to `RUNNER_START` event handler which allows to trigger and subscribe to any other events via this runner
* Fixed `flat` reporter which incorrectly counts statistics (`total`, `passed`, `failed` e.t.c) when several events were triggered for the same test (for example, `TEST_FAIL` after `TEST_PENDING`)

## 0.15.0 - 2016-10-10

* Throw an error if tests have the same title

## 0.14.0 - 2016-10-05

* Added configparser which is intended to verify configuration file and provides an opportunity to override config values through cli and environment variables
* Show fallen tests at the end of the reporter
* Added file path to the fallen tests at the end of the reporter
* Show correct errors which might be occur by connecting plugins
* Fixed bug with double slashes in meta url

## 0.13.0 - 2016-09-07

* Show tests in reports if they were skipped by the HERMIONE_SKIP_BROWSERS
environment variable
* Fixed files read error, when files in specs were specified as string.

## 0.12.0 - 2016-08-22

* Added passing of execution context to a browser instance in tests (see the [documentation](https://github.com/gemini-testing/hermione/blob/v0.12.0/README.md#execution-context) for more details)
* Added `SESSION_START` and `SESSION_END` events
* Fix: do not launch browsers for skipped tests

## 0.11.4 - 2016-08-11

* Switch to webdriverio@4.2.4

## 0.11.3 - 2016-08-11

* Switch to webdriverio master with `screenshotOnReject` option

## 0.11.2 - 2016-08-08

* Fix: throw error on incorrect path to test suites
* Fix: save whole url in meta info

## 0.11.1 - 2016-08-05

* Switch to the stable webdriverio version (screenshots will not be saved on reject now)

## 0.11.0 - 2016-08-01

* Added capability to run tests matched by masks

## 0.10.0 - 2016-08-01

* Added test metainfo access methods to webdriverio
* Save latest url opened by webdriverio in metainfo

## 0.9.1 - 2016-07-12

* Passthrough `screenshotOnReject` option to `webdriverio`

## 0.9.0 - 2016-07-12

* Added event `SUITE_FAIL` which is emitted instead of event `ERROR` when `before all` hook fails.

## 0.8.1 - 2016-07-04

* Added environment variable [HERMIONE_SKIP_BROWSERS](https://github.com/gemini-testing/hermione/blob/v0.8.1/README.md#hermione_skip_browsers).

## 0.8.0 - 2016-06-30

* Update webdriver.io to 4.1.0
* Decrease default waitTimeout value to 1000 ms

## 0.7.0 - 2016-05-12

* Added [skip API](https://github.com/gemini-testing/hermione/blob/v0.7.0/README.md#skip)
* Dropped supporting of node < 4.x

## 0.6.3 - 2016-05-04

* Update webdriver.io version to v4.0.4

## 0.6.2 - 2016-04-27

* Fixed retrying all suite tests on single test fail

## 0.6.1 - 2016-04-01

* Fixed crash on attempt to retry test.

## 0.6.0 - 2016-03-30

* Supported configuration of `specs` for certain browsers (see [#9]).
* Added option `--grep` for selecting specific tests (see [#15]).
* Improved documentation: translated from Russian to English and updated several sections.
* Fixed crash when enabling debug mode (see [#10]).

## 0.5.3 - 2016-03-04

* Correct exit code when config file is corrupted

## 0.5.2 - 2016-02-20

* Avoid `possible EventEmitter memory leak detected` warning in signalHandler
* Fix session ids in reporters

## 0.5.1 - 2016-02-18

* Fixed `NoSessionIdError` in parallel run

## 0.5.0 - 2016-02-17
* Plugin support added
* Retry logic added
* Better error logging
* Fixed `.only` option for tests
* Quit browsers on `Ctrl + C`

## 0.4.0 - 2016-01-28

* `capabilities` renamed to `desiredCapabilities`

## 0.3.3 - 2016-01-28

* `webdriverio` switched to v3.4.x version

## 0.3.2 - 2016-01-15

* Up lodash to version with `defaultsDeep`

## 0.3.1 - 2016-01-15

* Avoid 'possible EventEmitter memory leak detected' warning

## 0.3.0 - 2016-01-15

* `webdriverio` switched to master branch
* Allways show errors in logs
* Do not save screenshots on webdriver error by default
* Ability to set mocha options in config
* Up q-io and q version to 2.x

## 0.2.0 - 2016-01-13

* Add ability to run tests in specific browsers
* Allow unknown option for cli

## 0.1.0 - 2016-01-12

* Initial release

[#15]: https://github.com/gemini-testing/hermione/pull/15
[#10]: https://github.com/gemini-testing/hermione/pull/10
[#9]: https://github.com/gemini-testing/hermione/pull/9
