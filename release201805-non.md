 ****Draft****  -- 201805 - NON - Consensus Changing Release
 
  *(To the team... Feel free to copy and use this page note)*




***
***

# BitShares Core Release 2.0.180205
@oxarbitrage release this on...

Note:

***

### Assets
- BitShares-Core-2.0.180205-x64-cli-tools.zip
- Source code(zip)
- Source code(tar.gz)

***

## Security


## Bugfixes
* Fixed: `get_ticker` should return data time but not request time #863 (Fixed by #871)
* Fixed: Operation_history_id mismatch among nodes #585
* Fixed: sign_builder_transaction sometimes does not work #864 #865

## New features and improvements
* Implements BSIP31-34: Market engine  #641,#184, #59, #829, #830, #338 #343 #453 #606 #625 #649
* Implement BSIP26: Refund order creation fee in original paid asset when order is cancelled #604
  - Implement BSIP26 Refund original fee #627
  - Replaces #623. PR for #604
* Implement BSIP38: add target CR option to short positions #834
  - This is PR for #834 (BSIP38: add target_cr option to call order #834)


## Other changes & Updates
* Added: Mmessage to FC_ASSERT in application.hpp #869
* Added: Parameters to configure log rotation #805 #840
* Changed: `list_assets` API limit to 101 #862
* Fixed: Dump call stack on segmentation fault #727
* Fixed: Feed expiration integer overflow issue #888 #892
* Fixed: Handle acc_trx_his_object in get_relevant_accounts #816
* Fixed: History ids #873
* Fixed: Mac build: Template instantiation #817
* Fixed: MacOS memory access violation #813
* Fixed: Namespace Collision on bind in test #801
* Moved node and application implementations to header file #804


## Contributors in this release:
* @abitmore
* @pmconrad
* @xeroc
* @oxarbitrage
* @ryanRfox
* @jmjatlanta
* @ihla


## SHA256 Checksum
* `BitShares-Core-2.0.180205-x64--cli-tools.zip `: Windows 

