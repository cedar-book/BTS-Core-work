# BitShares Core TESTNET Release: test-2.0.180525  



#### TESTNET Protocol upgrade (Hard fork) time is scheduled at `Thu, 31 May 2018 14:00:00 UTC`.

**Testnet nodes (especially witnesses and public seed nodes and API nodes) please upgrade in time (before the scheduled time).**

Github: https://github.com/bitshares/bitshares-core/releases/tag/test-2.0.180525

---

##Details about this release:

#### 1. Protocol upgrade (hard fork) related:
* [Bugfix #922 / #931 / #970] Fixed missing checks when updating a smart coin's `bitasset` options E.G. force settlement delay, backing asset ID or etc;
* [Bugfix #935] Fixed missing margin call checks introduced in fix for #868 and #890 in last testnet release.
* [Bugfix #942] Fixed missing asset authorities check for "from" account when claiming from a withdraw permission.

#### 2. Other updates (including the ones done in last testnet release but not included in the release notes)

* [FC repository PR #36] Support Boost 1.64-1.65
* [FC repository PR #43] Fixed a memory leak issue in TCP socket destruction
* [FC repository PR #44] Fixed Diffie-Hellman shared key computation (related to memo encryption)
* [PR #938] Fixed an issue that may cause the node to store incorrect block ID to disk when switching forks
* [Issue #582, PR #813] Fixed macOS witness node crash issue when being used as an API server
* [Issue #776, PR #816 / #955] Fixed missing notification to RPC clients when changes occurred on some types of objects
* [Issue #888, PR #954] Fixed an integer overflow issue when checking whether a price feed has expired
* [Issue #864, PR #865] Fixed a `cli_wallet` transaction signing issue when creating proposals with transaction builder
* [Issue #859, PR #801 / #817] Fixed macOS and Ninja build errors introduced in last release
* [Iuuse #136, PR #928] Fixed an asset supply calculation error in test case
* [Issue #805, PR #840 / #919 / #937] Improved logging level and messages; added logging options about log-rotation
* [Issue #943, PR #869 / #945] Improved a few assertion error messages
* [Issue #727, PR #880] Added stack trace printing when node crashes (only for boost 1.65)
* [Issue #878, PR #927] Made number of IO threads configurable (can be manual or auto)
* [Issue #862, PR #872] Improved pagination of `list_assets` node API
* [Issue #863, PR #871] Node `get_ticker` API now returns time stamp of latest block instead of server time
* [Issue #811, PR #861] Added `get_full_account` command/API to `cli_wallet`
* [PR #850] Removed unused asset cache from `cli_wallet`
* [PR #918] Fixed in-code documentation for `set_desired_witness_and_committee_member_count` command/API in `cli_wallet`
* [PR #804] Refactored `node.cpp` and `application.cpp` for easier testing
* [PR #851 / #853 / #854 / #855] Fixed several compiler warnings

## Contributors in this release:
* @abitmore
* @pmconrad
* @xeroc
* @oxarbitrage
* @jmjatlanta 
* @ryanRfox

***
