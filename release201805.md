## ****Draft****  -- 201805 - Consensus Changing Release
*open*
- Review all new FC_ASSERT added to next hardfork release #679
- Clear price feed data after updated a bitAsset's backing asset ID #868
- Fix for Issue 868 - Reset feeds when changing the backing asset from one asset to another #882
- Should update median feeds after feed_lifetime_sec changed #890
- Issue 890 - update median feeds after feed_lifetime_sec changed #891

***
***

# BitShares Core Release 2.0.180205
@oxarbitrage release this on...

Note:


***

(.. not sure which group)
* Rounding issue when matching orders #342


***

### Assets
- BitShares-Core-2.0.180205
- Source code(zip)
- Source code(tar.gz)


## Security fixes
* BSIP 29: Require owner key for change of asset-issuer #199
  - PR #599

## Critical Bug Fixes

## New features and improvements

* BSIP27: OP for issuer to reclaim fee pool funds #188
* BSIP30: Disallowed increasing debt when updating short position (BSIP30 part 2) #827, #672
* BSIP35: Mitigate rounding issue when matching orders #830
  -  cherry-picked from #641, including changes related to #132, #184, #342 and BSIP35: Mitigate Rounding Issue On Order Matching
* BSIP36: Clear expired feeds on maintenance interval #889
  - New PR for issue: #518, refactored from PR #832
  - Clean up bitasset_data during maintenance #518
* BSIP37: Allowed new asset name to end with a number (BSIP37) #705, #620
* Implements BSIP31-34: Market engine  #641,#184, #59, #829, #830, #338 #343 #453 #606 #625 #649
* Implement BSIP26: Refund order creation fee in original paid asset when order is cancelled #604
  - Implement BSIP26 Refund original fee #627
  - Replaces #623. PR for #604
* Implement BSIP38: add target CR option to short positions #834
  - This is PR for #834 (BSIP38: add target_cr option to call order #834)

## Bugfixes
* Fixed: Black swan detection checks short position with lowest call_price but not lowest collateral ratio #649
* Fixed: Inconsistent sorting of call orders between matching against a limit order and a force settle order #343
* Fixed: Margin call order fills at price of matching limit_order but not at a price related to itself or settlement_price #338
* Fixed: Multiple limit order and call order matching issue #453, #537
* Fixed: Potential erratic order matching issue involving margin call orders #625
* Fixed: Potential something-for-nothing fill bug #184, #338.#342, #505
* Fixed: Unable to propose a proposal with an `approve_proposal` operation #214, #658, #492
* Fixed: Undercollateralized short positions should be called regardless of asks #606, #625, #641
* Fixed: Virtual operations should be excluded from transactions #588
  - PR #591

## Other changes & Updates
* Allowed updating a call order to higher collateral ratio #655, #583
* Asset claim pool operation #572
* Asset update issuer operation #599
* Cleaned feeds at maint time #598
* Cleaned up HF409 related code #712
* Created more test cases for BSIP 35 #883
* Fixed #214 #841
  - Revised HF protection for #214 with additional test scenario #857
* Fixed #588 Virtual operations should be excluded from transactions #698
* Review and test something-for-nothing check #132, #338, #342

## Contributors in this release:
* @abitmore
* @pmconrad
* @xeroc
* @oxarbitrage
* @ryanRfox
* @alexpmorris 


## SHA256 Checksum
* `BitShares-Core-2.0.180205-x64--cli-tools.zip `: Windows 


