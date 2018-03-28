# BitShares Core Release 2.0.182803

@oxarbitrage release this on...

## Security
* Reviewed all new `FC_ASSERT` added to next milestone #678

## Features and Improvements
* Added API's to get `withdraw_permission` objects related to an account https://github.com/bitshares/bitshares-core/issues/611 - https://github.com/bitshares/bitshares-core/pull/676
* Added application option to disable `notify_remove_create` parameter in `set_subscribe_callback` API https://github.com/bitshares/bitshares-core/pull/725
  - Temporarily removed enable-subscribe-to-all option (*Uncomment when GUI is ready) https://github.com/bitshares/bitshares-core/issues/740 - https://github.com/bitshares/bitshares-core/issues/743
* Added assertion messages in account evaluator. https://github.com/bitshares/bitshares-core/issues/691 - https://github.com/bitshares/bitshares-core/pull/736
* Added `broadcast_transaction` method for broadcasting transaction signed by … #656
* Added CLI wallet test framework #675
* Added `get_top_markets` API #512, #737
* Added SSL, Boost and websocket to Version commands #579, #610
* Added New plugin and API: grouped orders #639, #662
* Added `withdraw_permission` API calls #676
* Added Travis-CI build status iconds for branches: master, develop, hardfork, testnet and bitshares-fc #748
* Added New plugin: elasticsearch objects #500
* Changed `get_account_history` API call #628 (for issue #613)
* Enabled Travis-CI for develop branch #748
* Issue491: Minor delta_debt amount check issue in `call_order_update_evaluator` #609
* Partially fixed Issue #151: CLI account caching #640
* Port plugin sanitization code from Steem to BitShares #468 #660
* Pushed settle_order changes if subscribed to market #747 #745

## Bugfixes
* Fixed #436 object_database created outside of witness data directory #689
* Fixed add_secondary_index on gcc7 #761
* Fixed broken HTTP headers in Elasticsearch requests #653
* Fixed Cherry-pick websocketpp for Linux kernel higher than 4.4.0 #701
* Fixed CLI `account_update` related commands #576
* Fixed cull-small issue in `check_call_orders` #697
* Fixed #721 disconnect a peer due to request timeout #722
  - Bug in terminate_inactive_connections_loop function in node.cpp #721
* Fixed `fee_refund_test fails` #615
* Fixed JSON #714 - Updated serialization for extension class #723
* Fixed object_database created outside of witness data directory when witness_node is started with `--replay` #436
* Fixed outdated header comments in egenesis_brief.cpp.tmpl and egenesis_full.cpp.tmpl #728
* Fixed some more code sanitizer errors #644
* Fixed variant conversion issue in get_full_account #763

## Bitshares FC

* Replace readline library https://github.com/bitshares/bitshares-fc/pull/12 - https://github.com/bitshares/bitshares-fc/pull/16 - https://github.com/bitshares/bitshares-fc/pull/17
* Added Doxygen support to project https://github.com/bitshares/bitshares-fc/pull/12
* Fixed JSON parsing https://github.com/bitshares/bitshares-fc/pull/15
* Update websocketpp submodule to a forked and patched version(After merged, need to run `git submodule sync --recursive` to update local repository) https://github.com/bitshares/bitshares-fc/pull/18 
* Fix default standard c++ at CMakeLists https://github.com/bitshares/bitshares-fc/pull/19/ 
* Fix serialization https://github.com/bitshares/bitshares-fc/pull/20
* Fix variant https://github.com/bitshares/bitshares-fc/pull/21
* Fix class serialization https://github.com/bitshares/bitshares-fc/pull/22
* Fix MacOS build https://github.com/bitshares/bitshares-fc/pull/24 - https://github.com/bitshares/bitshares-fc/pull/25
* Add Travis support and fix output https://github.com/bitshares/bitshares-fc/pull/27 - https://github.com/bitshares/bitshares-fc/pull/28 - https://github.com/bitshares/bitshares-fc/pull/30 - https://github.com/bitshares/bitshares-fc/pull/31
* Remove unused c++14 flag in CMakeLists https://github.com/bitshares/bitshares-fc/pull/32
* Skip editline in windows build https://github.com/bitshares/bitshares-fc/pull/34


## Other changes
* Changed to intense block_tests #718
* Replaced readline library, Issue 673 #685 (-for peer review. Submitted a PR to fc repo: bitshares/bitshares-fc#16 #17.)
* Removed unused transaction_object.cpp #667
* Removed `by_feed_expiration` index from `asset_bitasset_data_object` #652
* Removed redundant template func add_secondary_index #749
* Removed unused index.cpp file #638


## Contributors in this release:
* @abitmore
* @pmconrad
* @xeroc
* @oxarbitrage
* @jmjatlanta 
* @cifer-lee
* @aautushka 
* @ihla
* @marcialvieira
* @ryanRfox

## SHA256 Checksum
* `BitShares-Core-2.0.180203-x64--cli-tools.zip `: Windows 


