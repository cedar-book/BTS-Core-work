# BitShares Core Release 2.0.1808


### Assets

- BitShares-Core-2.0.1808-macOS-cli-tools.tar.gz
- BitShares-Core-2.0.1808-x64-cli-tools.zip
- Source code (zip)
- Source code (tar.gz) 

## Security fixes
- CLI wallet: updated choice of range proof params in cli wallet reveals transaction magnitude to very narrow range for Blinded Transfers (issue #480 / PR #1117 #1227)

## API changes
- Removed crypto_api from default list of allowed APIs. (issue #1123 / PR #1125)
- Changed default `max-ops-per-account` value to 100, impacts account history (#1120)
- Added `get_account_limit_orders` database API to query for open orders of one account in one market #463 #849 #1163
- Added `get_asset_count` API to return total number of available assets #688, #1159
- Added `get_transaction_hex_without_sig` API get serialized transaction hex without `signatures` field (issue #1013 / PR #1038)
- Added support for account name as parameter for all API calls #969 #989 #1164 #1168 #1152 #1155
- Added `fail_reason` field to proposal object #730, #1036
- Retroactively deducted witness `missed_blocks` caused by chain halts #1087

## New features and improvements
- Added Openssl 1.1 and Ubuntu 18.04 support (issue #835 / PR #559 #921 #1008 https://github.com/bitshares/bitshares-fc/pull/7)
  - Fixed invalid use of incomplete type `BIGNUM {aka struct bignum_st}` #327
- Added `witness_node` startup option `--enable-standby-votes-tracking` to track votes of standby witnesses and committee members #987, #1191, #1211
- Added `cli_wallet` startup option `--suggest-brain-key` to generate keys without connecting to a witness_node #1011, #1039
- Added `quit` command to `cli_wallet` #1104, #1050 https://github.com/bitshares/bitshares-fc/pull/63
- Improved witness_node performance for generating blocks, resyncing and replaying
  - Improved account maintenance (vote tally) performance (issue #803/ PR #1085)
  - Improved performance of `database::update_expired_feeds()` and global object getters #1093 #1180
  - Slightly improved price comparison performance #1094 #1124
  - Added index on `short_backing_asset`, better performance for updating asset (Issue #960 / PR #1019)

### Docker File
- Changed default docker p2p port to 1776, fixed p2p port to match Dockerfile #1226, #1078
- Fixes to make Docker containers shutdown gracefully #1077 #1115
- Fixed Docker Cloud Build Failing Due to Compile Time #1221 #1222
- Modified Dockerfile to work with new docker cloud version (0.10.1) #1075
- Updated testnet Branch to Include Latest Dockerfile #1074

### Elasticsearch
- Elasticsearch refactor #1103 #1201
  - Add auth to communicate with the ES database with `--elasticsearch-basic-auth` startup option.
  - Custom index names with `--elasticsearch-index-prefix` startup option.
  - Removed `--elasticsearch-logs` startup option
  - Better error handling: if there is an error when sending data to ElasticSearch, plugin will stop processing blocks and keep trying, and it resumes when connection is back at the same place. #681
  - add operation_id_num for easier filtering.
  - Fill orders data in additional for easy volume.
  - Test cases framework. #1047
  - Make full use of common functions in the 2 plugins(utilities).
  - flush ES database on every block when node is in sync to improve real time user experience. #1137
- Updated documentation https://github.com/bitshares/bitshares-core/wiki/ElasticSearch-Plugin

## Bugfixes
- Fixed CLI `get_account_history` pagination issue (duplicate ops when `limit` great than 100) #1176, #1177, #1179
- Fixed `cli_wallet` crashes for macOS 10.13.5 #1127 https://github.com/bitshares/bitshares-fc/pull/60
- Fixed "log file of current hour gets overwritten by default" #809 https://github.com/bitshares/bitshares-fc/pull/56
- Fixed 2 minor bugs in snapshot plugin #1185
- Fixed object database exception handling when built with Boost 1.66 (#852 #1126 #1161)
- Enable `boost::stacktrace` correctly https://github.com/bitshares/bitshares-fc/pull/66

## Other changes
- Integrated SonarCloud into travis build (issue #836 / PR #1081 https://github.com/bitshares/bitshares-fc/pull/49)
- Added `USE_PROFILER` option to Cmake to enable profiling #1119
- Added `OPENSSL_CONF_SOURCE` variable for building in Windows https://github.com/bitshares/bitshares-fc/pull/59
- Added cli_tests to Travis-CI #1156
- Added `asset_api_tests` #1202
- Added new seed node by bangzi #1130 #1138
- Changed default `core_exchange_rate` quote asset in order to create asset more easily #1132
- Updated node.cpp, check attacker/buggy client before updating items ids #1007
- Optimized `find()` call in P2P code #1090, #1091
- Refactored `get_impacted_account_visitor`, removed duplicate code from impacted.cpp #845 #1073
- Refactored `cancel_all_subscriptions` for better performance and consistency #762 #1009 https://github.com/bitshares/bitshares-fc/pull/50
- Changed `push_proposal exception` log level to warn #1146
- Cleaned up Balance evaluator code #1150
- Cleaned up `get_named_account_balances` code #1154 , #1135
- Cleaned up logging in account.cpp #1010
- Cleanup up a visitor struct in static_variant.hpp https://github.com/bitshares/bitshares-fc/pull/58
- Removed obsolete constants (issue #1034 / PR #1072)
- Removed unused "smaz" compression #986 https://github.com/bitshares/bitshares-fc/pull/51
- Remove fc bz2 unused linkage https://github.com/bitshares/bitshares-fc/pull/52
- Removed double assert in `object_id_type` constructor #1128
- Removed protocol.hpp #1197, #1200
- Backported EOS PR 3560 replace assert in FC::crypto #992 https://github.com/bitshares/bitshares-fc/pull/54
- Backported EOS PR 3240 HTTP performance improvement, added move-semantic-version `set_body` function #999 https://github.com/bitshares/websocketpp/pull/1 https://github.com/bitshares/bitshares-fc/pull/65
- Updated test case for `time_point_sec::to_iso_string`, detect boost version #597 https://github.com/bitshares/bitshares-fc/pull/67
- Fixed Performance sucks at first block after a long sequence of missed blocks #1086 #1087
  - witness `missed_blocks` count no longer increases due to chain halt (retroactive change)
- Fixed cli_tests websocket port binding #1178 #1187
- Fixed RPC logging level inconsistency #929 https://github.com/bitshares/bitshares-fc/pull/62
- Fixed wallet in-code docs, suppressed compiler warnings  #1015 #1181 #1129 #1199 #1190
- Updated `asset_object::amount_to_string` implementation for slightly better performance #1012
- Updated system requirements into Documents #1107 #1108
- Updated README.md document #1121, #1166, #1212


## Contributors in this release:

- @pmconrad
- @abitmore
- @oxarbitrage
- @jmjatlanta
- @cogutvalera / @nanomobile
- @cifer-lee
- @ryanRfox
- @nathanhourt
- @christophersanborn
- @xeroc
- @xiangxn
- @RichardWeiYang
- @Zapata
- @cwyyprog
- @Tydus

## SHA256 Checksum	

