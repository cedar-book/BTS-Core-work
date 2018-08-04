## ****Draft****

# BitShares Core Release 2.0.180328

### Assets
- BitShares-Core-2.0.180328
- Source code(zip)
- Source code(tar.gz)

## Security
* Reviewed all new `FC_ASSERT` added to next milestone #678

## Features and Improvements
* Added API's to get `withdraw_permission` objects related to an account #611
* Added application option to disable `notify_remove_create` parameter in `set_subscribe_callback` API #725
  - Temporarily removed enable-subscribe-to-all option (*Uncomment when GUI is ready) #743 
  - Set default value of `application_options::enable_subscribe_to_all` to `true` #740
* Added assertion messages in account evaluator. #736
* Added `broadcast_transaction` method for broadcasting transaction signed by … #656
* Added CLI wallet test framework #675
* Added `get_top_markets` API #512, #737
* Added SSL, Boost and websocket to Version commands #579, #610
* Added New plugin and API: grouped orders #639, #662
* Added New plugin: elasticsearch objects #500
* Added `withdraw_permission` API calls #676
* Added Travis-CI build status iconds for branches: master, develop, hardfork, testnet and bitshares-fc #748
* Changed `get_account_history` API call #628 (for issue #613)
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


## Other changes
* Changed to intense block_tests #718
* Replaced readline library, Issue 673 #685 (-for peer review. Submitted a PR to fc repo: bitshares/bitshares-fc#16 #17.)
* Replace readline library #673 (-bitshares/bitshares-fc#14)
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
* `BitShares-Core-2.0.180328-x64--cli-tools.zip `: Windows 
