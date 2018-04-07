(in this example, you need to have **CLI Wallet** commond window ready at this point to type in a command.  **server** and **Witness_node** (Full node) .  have to have a **lifetime membership** to register an account.)

---

### Contents 

1. Create a brain Key and derive a private/public key pair
2. Create an Account     
3. Register an Account



## 1. Create a brain Key and derive a private/public key pair
Use the `suggest_brain_key` command in the CLI Wallet. 

**example**

    >>> suggest_brain_key
    {
    "brain_priv_key": "FILINGS THEREOF ENSILE JAW OVERBID RETINAL PILULAR RYPE CHITTY RAFFERY HANDGUN ERANIST UNPILE TWISTER BABYDOM CIBOL",
    "wif_priv_key": "5JVrt2921aikA7QP5ZCtR2sJh4wbEnsHsK6qo67Shnk9ArKMzNT",
    "pub_key": "BTS7D8jpQ2UwaQxqKyGpuhFQ9LBugCNxDhE7UN2jqgjVQgzG7zo9n"
    }

The hierarchy for these values goes like this::

     HASH(brain_priv_key) -> wif_priv_key
     HASH(HASH(brain_priv_key)) -> pub_key

**`suggest_brain_key`**

|   return item       |  note            |
| ------------------- |---------- |
| "brain_priv_key"    |  You will be able to recover your required keys to access your account and/or funds. |                           
| "wif_priv_key"      |  private key  (i.g., owner key) |                            
| "pub_key"           |  public Key  |                           

> Note: Even though suggest_brain_key shows only one private key that will be used for the **owner authority** most wallet implementations will derive an additional second private key to be used for the **active authority**!


## 2. Create an Account
If you want to create and register a new account on your own because you have the funds in another account and don’t want someone else involved, you can make use of the command `create_account_with_brain_key`::

    >>> create_account_with_brain_key <brain_key> <account_name> <registrar_account> <referrer_account> <broadcast>

**example**

    >>> create_account_with_brain_key "FILINGS THEREOF ENSILE JAW OVERBID RETINAL PILULAR RYPE CHITTY RAFFERY HANDGUN ERANIST UNPILE TWISTER BABYDOM CIBOL" mywallet myfunds anonymous true

**`create_account_with_brain_key`**

|  parameter          |  note     |
| ------------------- |---------- |
| [brain_key]         | "brain_priv_key" value - created by the `suggest_brain_key` command.  |                           
| [account_name]      |   (e.g., mywallet)  |                            
| [registrar_account] |   (e.g., myfunds)     |                           
| [referrer_account]  |  (e.g., anonymous )     |                            
| [broadcast]         | (e.g., true)     |


## 3. Register an Account
In order to register an account, we need an other account that has enough funds to pay the fee for the registration transaction. This account will be called `registrar_account`. Another account `referrer_account` can be registered that will get `referrer_percentage` of the referral bonus program. Any registered account can take the role of the referrer. Hence we here say that user `anonymous` has referred us. 

    >>> register_account <name> <owner_pubkey> <active_pubkey> <registrar_account> <referrer_account> <referrer_percent> <broadcast>

**example** 

 We register a new user called mywallet, use the pubkey derived above and let our account myfunds pay the fee::

    >>> register_account mywallet BTS7D8jpQ2UwaQxqKyGpuhFQ9LBugCNxDhE7UN2jqgjVQgzG7zo9n BTS7D8jpQ2UwaQxqKyGpuhFQ9LBugCNxDhE7UN2jqgjVQgzG7zo9n myfunds anonymous 100 true

**`register_account`**

|   parameter          |  note     |
| ------------------- |---------- |
| [name]         | (e.g., mywallet)   |                           
| [owner_pubkey]      |  "pub_key" value - created by the `suggest_brain_key` command in the CLI Wallet.  |                            
| [active_pubkey] |  "pub_key" value - created by the `suggest_brain_key` command in the CLI Wallet. |                           
| [register_account]  | pay the fee for the registration transaction.  (e.g., myfunds)   |                            
| [referrer_account]  |  (e.g., anonymous) | 
| [referrer_percentage]  |  (e.g., 100)      |                            
| [broadcast]         |  (e.g., true)      |


>Note:Note that in order to register an account, the registrar (here: myfunds) needs to be a lifetime member!

>Nate:If you want to register the account of someone else, all you need is the public key.


