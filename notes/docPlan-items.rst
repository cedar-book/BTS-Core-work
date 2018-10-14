.. _my-plan:

***********************
Documentation Plan
***********************
(I am going to work on or have been working in.)

- Update "exchange_single_node.md" --> "exchange_single_node.RST"
- 
- add information list pages (api, database_api(classes/struct) methods names and descriptions. index page)
- Transactions processes (elements flows charts?)

  - validation, history, blocks, ...
  
- Flowcharts

  - transaction.hhp
    - transaction
    
    - (get_required_autotities, signed_transaction, sign, minimize-required_signatures, get_required_siguratures, verify_authority, get_signatures_keys, sign_state, ..)
  
  - application_impl.hxx
  
    - (get_api_access_info, set_api_access_info, has_item, handle_block, handle_transaction, is_included_block, get_block_ids, get_blockchain_synopsdis, )
    
  - api.cpp
    
    - (login, enable_api, network, broadcase_api, on_applied_block, broadcase_transaction, broad_transaction_synchronous, brodcast_block, broadcast_transaction_with_callback, get_info, add_node, get_fill_order_history, get_account_history, get_account_history_operations, get_relative_account_history, get_account_history_by_operations, get_market_history,..)
  
- add contents to Totorials and FAQs

- Multi-sig UI - How to use?
- directory structures and files after the installation (node/wallet) 

  - (i.e., datadir... )

- create a wiki legacy folder and create pages. [10/12: will finish soon.]
- Test cases - categories, test cases name list (i.e., index)


|

-------



**These items are some documentation work items that I could thought about. 

Items
========================

1. Maintenance 
---------------
* updates/maintain current documentations (dev/how)

  - update,fix...

2. Improvement
-------------------
* improve tutorials and FAQs contents
* add links to each API calls (in the API section) to open a Doxygen location directory (?)
* glossary (General and BitShares) lists

  - add more terms


3. flowcharts
-------------------------

* create flowcharts of some processes (flows / layers)


4. Find examples (how to use)
--------------------
* where/how 'operations' have been used in the BitShares application code (programs) 

  - find sample programs areas (class/function) from the existing code (*including particular  operations/components)
  - examine
 
* how 'objects' have been used in in the BitShares functions (programs) 

  - show example coding areas
  - examine
  
* where/how classes/functions/methods have been used in the BitShares application code 

  - find sample program areas from the existing code
  - examine 
  
* Create functions list for users to find easily

  - file, name, params, short description... (*seek - better way to appeal and let users know what BitShares-Core offers)
  - (wallet, witness node, node,?)
  

5. plugins
----------------------
* introduce concept (*Alfredo's presentation material)
* how to create

  - "hello world" 
  
* find each sample cording area (how it has been used in programs) 
  
  - examine and draw a flow
  
  
6. Create and Add contents
------------------------  
* improve the System Components Elements section

  - add more features and definitions (*think about better grouping/indexing) 

* ~~look into BitShares-FC components~~ (?)
* "hello world" examples of some procedures (?) 
* add Knowledge Base section and create the contents 

  - add wiki legacy pages (.md --> .rst)
  - (e.g.) add documented issues or information that need to be documented
  
9. Other
-----------
 
* gather BitShares discussion items (from issues or BSIP)(?)

* wallet functionalities (code/library) list to find/learn easily

  - features/functions (+ short description) 
  
* witness node functionalities (code/library) list to find/learn easily

  - features/functions (+ short description) 

-----------------

--------------------

7. Look into the issues (from users)
------------------------
* BitShares-Core

  - documentation of issues
  
* dev.bitshares.works

  - update/improvement
  
* how.bitshares.works

  - update/improvement

----------------------------

**BBF - User Guide**

8. BitShares-UI
---------------------
(Probably, I can manage the upper level User guide because I am not BitShares-UI team. BitShares-UI team should add/create their version of User Guide(?))

* update

  - somehow/someone need to manage UI User Guide section
  - BitShares-UI repository issues - 'Documentation' tag to find out what need to be updated. 
  
|
---------------------


TSugimoto
  


|

