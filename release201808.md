## BitShares Core Release 2.0.1808


### Assets




### Security fixes
- Updated Choice of range proof params in cli wallet reveals transaction magnitude to very narrow range for Blinded transfers (closed by #1117) #480
- Updated Range proof mantissa minimum bit length (Fixed #480) #1117

### New features and improvements
- Added CLI startup option to only generate keys #1011, #1039
- Added exit or quit command to cli_wallet  #1104,#1050
- Added fail reason to proposal object #730, #1036
- Added `compile-time` option `TRACK_STANDBY_VOTES`-#987 #1140
- Added startup option to update votes for inactive objects in API nodes #987 
- Added startup option to track votes of standby witnesses and committee members #987, #1191, #1211
- Added support account names or ids in all API calls #989 , #969
- Fixed CLI `get_account_history` pagination issue #1176, #1177, #1179
- Fixed Openssl 1.1 support to compile bitshares-fc (ref bitshares-fc#7) (Replacement PR for #559) #921
- Fixed to use `get_account_from_string` in `get_account_limit_orders` - (for issue #1164) #1168
- Refactored `get_account_limit_orders` API account name support (this is fixed in #1168) #1164
- Added to return total number of available assets #688
- Fixed issue #688, add `get_asset_count` API #1159
- Implemented merge impacted into `db_notify`	#1073
- Improved account maintenance performance (PR for #803)	#1085
- Improved performance of `database::update_expired_feeds()` #1093
- Improved price comparison performance - Merged #1124. Closing. #1094
- Improved `update_expired_feeds performance` (PR for #1093, rebased from #1113) #1180
- Improved vote tally performance (affected maintenance block producing (#504) as well as overall sync/replay time) #803
- Integrated SonarCloud (More info: https://about.sonarcloud.io/.) - closed by #1081	#836
- Optimized P2P find() #1090

#### Docker File
- Changed default docker p2p port to 1776, #1226
- Fixed Dockerfile (fix #1221) #1222
- Fixed Docker Build Failing Due to Compile Time #1221
- Fixed to make Docker containers shutdown properly #1115
- Fixed p2p port to match Dockerfile #1078
- Modified Dockerfile to work with new docker cloud version #1075
- Updated testnet Branch to Include Latest Dockerfile		#1074

#### Elasticsearch
- Elasticsearch feature requests. #1103
- Elasticsearch refactor #1122
- Implemented Detect error on _bulk API on elasticsearch plugin #681
- Updated Elasticsearch refactor - added basic auth, `operation_id_num` , removed logs #1122
- Updated ElasticSearch test cases framework	#1047

### Bugfixes
- Fixed `cancel_all_subscriptions` API (Merged #1009) Closing. #762
- Fixed `cli_wallet` throws error and crashes - OS: macOS 10.13.5 #1127
- Fixed CLI `get_account_history` pagination issue - PR for #1176. #1177
- Fixed `fc::time_point_sec::to_iso_string` #597
- Fixed `get_account_history` return duplicate ops #1176
- Fixed Log file of current hour gets overwritten by default(Fixed with #1104) #809
- Fixed Performance sucks at first block after a long sequence of missed blocks (Resolved via #1087)		#1086
- Fixed Short-cut long sequences of missed blocks (Fix #1086) #1087
- Refactored `cancel_all_subscriptions` (#762) #1009

### Other changes
- Added `asset_api_tests` (for the branch) #1202
- Added API to query for open orders of one account in one market #849
- Added Build Error Template (Fix for #1021) #1030
- Added default quote `asset_id` to 1.3.1	#1132
- Added index on `short_backing_asset` (Issue #960) #1019
- Added Issue Templates #895
- Added new seed node by bangzi (Rebased #1130)	#1138
- Added voting test (Testcase for #1191) #1211
- Bumped FC (FC will be bumped as part of #1104)(Travis-CI failure will be fixed by #1187) #1189
- Cleaned code, bump FC (Assigned value is garbage ) #986
- Cleaned Balance evaluator code 	#1150
- Changed BTS to GRAPHENE_SYMBOL for testnet cli_test #1227
- Changed `push_proposal exception` log level to warn #1146
- Cleaned up `get_named_account_balances` code #1154 , #1135
- Cleaned up logging in account.cpp #1010
- Fixed #809 issue, open log file in append mode #1102
- Fixed 2 bugs reported by sonarqube #1185
- Fixed Back-port EOS PR 3560 replace assert in FC::crypto (Fixed with #1104.)#992
- Fixed CLI test failure: Underlying Transport Error (Travis-ci)#1178
- Fixed cli_tests websocket port binding (PR for #1178.)#1187
- Fixed cli_wallet tests failing (closed by #1155 and #1156) #1152
- Fixed compiler warnings	#1129
- Fixed `fc::time_point_sec::to_iso_string`  (this is for tracking and testing) #597
- Fixed invalid use of incomplete type ‘BIGNUM {aka struct bignum_st}’ #327
- Fixed New API: get transaction hex without `signatures` field -(Fix #1013) #1038
- Fixed Possible to generate a block that is too large (Closed via #1142.) #1136
- Fixed RPC logging level inconsistency (level=error, warn, and info) #929
- Fixed wallet in-code docs #1015
- Fixed wrong variable name in `vote_for_witness` (for #1152) 
  - (get_witness_by_account(voting_account); to get_witness_by_account(witness)) #1155
- Merged bump fc for openssl1.1 #1008
- Merged develop branch into release branch #1223,#1228
- Merged release branch back to to develop branch #1229
- Merged release branch into testnet branch #1225
- Merged Sonar integration into travis build  (Fixes #836)#1081
- Merged testnet_release branch into testnet branch #1230
- Minor optimization about price comparison #1094 #1124
- Optimized Backport EOS PR 3240 HTTP performance  (Added move-semantic-version `set_body` function) #999
- Removed crypto_api from default list of allowed APIs. (Fix for #1123)	#1125
- Removed double assert in `object_id_type` constructor #1128
- Removed needless find() in p2p	#1091
- Removed protocol.hpp #1197 ,#1200
- Suppressed compiler warnings in `database_api_tests` #1181
- Suppressed compiler warning on wallet API docs #1199
- Suppressed compiler warnings when generating wallet API docs #1190
- Updated [cosmetics]`get_impacted_account_visitor` defined in impacted.cpp and db_notify.cpp	#845
- Updated `asset_object::amount_to_string` implementation #1012
- Updated database_api.hpp minor (Moved get_account_limit_orders API from accounts section to markets/feeds section) #1163
- Updated Document - Ubuntu 18.04 Support #835,#1121. #1166, #1212
- Updated node requirements #1108
- Updated system requirements into Documents #1107
- Updated to get rid of obsolete constants - fix #1034,#1072


- Reverted "Capture Ctrl+C in cli_wallet when not in daemon mode #1193" #1220
  - -->> Capture Ctrl+C in cli_wallet when not in daemon mode (PR for #1193) #1207


### Contributors in this release:

- @pmconrad
- @abitmore
- @oxarbitrage
- @jmjatlanta
- @xeroc
- @ryanRfox
- @cifer-lee
- @ihla
- @zhuliting
- @Zapata
- @clockworkgr 
- @litepresence
- @startailcoon
- @nanomobile

	
	
	
### SHA256 Checksum	

