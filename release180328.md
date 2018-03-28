**This release contains several security fixes. All nodes please upgrade as soon as possible.**

Note:
* `libcurl-dev` is a dependency since release [2.0.171212](https://github.com/bitshares/bitshares-core/releases/tag/2.0.171212). For Ubuntu, use this command to install it:
  * `sudo apt-get install libcurl4-openssl-dev`
* The submodule remote URLs were changed in this release. To update an existing local repository, need to run additional `git submodule sync` and `git submodule update` commands:
```
git fetch origin
git checkout 2.0.180328
git submodule update --init --recursive # this command will fail
git submodule sync --recursive
git submodule update --init --recursive
```

## Security fixes
* Fixed JSON parsing issues in FC: https://github.com/bitshares/bitshares-fc/pull/15
* Fixed serialization issues in FC: https://github.com/bitshares/bitshares-fc/pull/20, https://github.com/bitshares/bitshares-fc/pull/22
* Fixed `variant` processing issues and logging issues in FC: https://github.com/bitshares/bitshares-fc/pull/21, https://github.com/bitshares/bitshares-fc/pull/28
* Fixed an invalid iterator dereferencing issue: https://github.com/bitshares/bitshares-core/pull/697
* Fixed a negative amount issue: https://github.com/bitshares/bitshares-core/pull/790

## New features and improvements
* Implemented `grouped_order` plugin with API, enabled by default in `witness_node`, so clients can get cleaner order book when there are lots of dust orders: https://github.com/bitshares/bitshares-core/issues/639, https://github.com/bitshares/bitshares-core/pull/662
* Implemented `es_objects` plugin to store "objects" in Elastic Search for easy querying: https://github.com/bitshares/bitshares-core/pull/500/
* Added API's to get `withdraw_permission` objects related to an account https://github.com/bitshares/bitshares-core/issues/611, https://github.com/bitshares/bitshares-core/pull/676
* Added `get_top_markets` API https://github.com/bitshares/bitshares-core/issues/512, https://github.com/bitshares/bitshares-core/pull/737
* Added `broadcast_transaction` CLI command/API for broadcasting transaction signed by cold wallet https://github.com/bitshares/bitshares-core/pull/656
* Added a `proposer` field (fee_paying account) in proposal object https://github.com/bitshares/bitshares-core/pull/608
* Settlement order changes will be pushed to client if subscribed to certain market https://github.com/bitshares/bitshares-core/issues/745, https://github.com/bitshares/bitshares-core/pull/747
* Added SSL, Boost and websocket to `--version` commands output https://github.com/bitshares/bitshares-core/issues/579, https://github.com/bitshares/bitshares-core/pull/610
* Refactored `get_account_history` API for better performance https://github.com/bitshares/bitshares-core/issues/613, https://github.com/bitshares/bitshares-core/pull/628
* Plugin sanitization https://github.com/bitshares/bitshares-core/issues/468, https://github.com/bitshares/bitshares-core/pull/661

## Bugfixes
* Fixed websocket connection issue in Linux when kernel higher than 4.4.0 https://github.com/bitshares/bitshares-fc/pull/18
* Correctly disconnect peers https://github.com/bitshares/bitshares-core/issues/721, https://github.com/bitshares/bitshares-core/pull/722
* Fixed broken HTTP headers in Elasticsearch requests https://github.com/bitshares/bitshares-core/pull/653
* Partially fixed CLI account caching issue https://github.com/bitshares/bitshares-core/issues/151, https://github.com/bitshares/bitshares-core/pull/640
* Fixed https://github.com/bitshares/bitshares-core/issues/436 object_database created outside of witness data directory https://github.com/bitshares/bitshares-core/pull/689


## Other changes
* Added Travis-CI integration https://github.com/bitshares/bitshares-core/pull/748, https://github.com/bitshares/bitshares-fc/pull/27
* Added Doxygen support to FC https://github.com/bitshares/bitshares-fc/pull/12
* Replaced readline library with editline https://github.com/bitshares/bitshares-fc/pull/14, https://github.com/bitshares/bitshares-fc/pull/16, https://github.com/bitshares/bitshares-fc/pull/17
* Added CLI wallet test framework https://github.com/bitshares/bitshares-core/issues/674, https://github.com/bitshares/bitshares-core/pull/675, https://github.com/bitshares/bitshares-core/pull/767
* Added assertion messages in account evaluator. https://github.com/bitshares/bitshares-core/issues/691, https://github.com/bitshares/bitshares-core/pull/736
* Fixed some code sanitizer errors https://github.com/bitshares/bitshares-core/pull/644
* Fixed C++ standard issue in FC CMakeLists https://github.com/bitshares/bitshares-fc/pull/19, https://github.com/bitshares/bitshares-fc/pull/32
* Fixed `fee_refund_test` https://github.com/bitshares/bitshares-core/issues/615, https://github.com/bitshares/bitshares-core/pull/616
* Fixed test cases in intense_tests and moved them to chain_tests https://github.com/bitshares/bitshares-core/issues/565, https://github.com/bitshares/bitshares-core/pull/718
* Fixed outdated header comments in egenesis_brief.cpp.tmpl and egenesis_full.cpp.tmpl https://github.com/bitshares/bitshares-core/issues/728, https://github.com/bitshares/bitshares-core/pull/734
* Removed unused files https://github.com/bitshares/bitshares-core/pull/667, https://github.com/bitshares/bitshares-core/pull/638
* Removed unused `by_feed_expiration` index from `asset_bitasset_data_object` https://github.com/bitshares/bitshares-core/issues/652, https://github.com/bitshares/bitshares-core/pull/654
* Cleaned up delta_debt amount check in `call_order_update_evaluator` https://github.com/bitshares/bitshares-core/issues/491, https://github.com/bitshares/bitshares-core/pull/609


## Contributors in this release:
* @pmconrad
* @abitmore
* @oxarbitrage
* @jmjatlanta 
* @xeroc
* @ryanRfox
* @aautushka 
* @ihla
* @marcialvieira
* @zhuliting
* @cifer-lee
* @tmfc
