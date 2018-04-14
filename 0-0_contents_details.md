*** This is DRAFT Detailed contents. will change to improve.  ****


## 0. About

## 1. Download & Installation
   - Links, Release, 
   - Ubuntu Linux
   - OS X
   - Windows
   - Windows - CLI Tools
      - How to 
      - Example Calls
   - Web and light wallet
   - tools, other repos for refer 

## 2. Accounts
   - Account
   - Account Registration
      - Create a brain Key and derive a private/public key pair
      - Create an Account
      - Register an Account

## 4. CLI Wallet
   - about
   - Cli-Tools for Windows (option)
   - Create a Cli Wallet and Open RPC port
      - Case 1: Connecting a Cli-Wallet - use the public API node
      - Case 2: Connecting a Cli-Wallet
      - Case 3: Connecting a Cli-Wallet - Public Testnet
      - Examples 
         - Issue any command available to the cli-wallet (Wallet APIs) 
         - construct a transaction manually
   - Gaining Access to Stake 
      - Creating Accounts -->Account Registration
      - Examples 
         - Send funds from faucet to alpha 
   - Network and Wallet Configuration
      - General 
         - Trusted Full Node:
         - Wallet
      - Secure 
         - Trusted Full Node:
         - Delayed Full Node:
         - Wallet
   - Tools
      - Monitoring Account Deposits with Python
      - NodeJS Monitoring Tool

## 5.1. Full Nodes (Witness Nodes)
   - Type of Witness nodes
      - non-block producing
      - block producing
   - How to launch the full node
   - Enabling Remote Procedure Calls (RPC)

## 5.2. Become an Active Witness
   - A Block Producing Witness
       - Requirements
       - Hardware Advice
       - Active Witness Duties
   - How to become a Block-Producing Witness
       - Run a local (non block producing) full node
       - Launch a CLI wallet
       - Gain Access to Stake
       - Register a new Witness Object
       - Configuration of the Witness Node
       - Verifying Block Production
       - Backup Server
       - Price Feeds

## 6. APIs
   - APIs two categories
      - Blockchain API
      - Wallet API
   - API Access Restrictions
   - Blockchain Specifications
      - Object and IDs
   - Calls
      - Remote Procedure Calls
         - Prerequisites
         - Call Format
         - examples
      - Websocket Calls & Notifications
         - Prerequisites
         - Call Format
         - Request API Access - steps
         - examples
   - Wallet APIs (**with examples!)
      - General Calls
      - Wallet Calls
      - Account Calls
      - Trading Calls
      - Asset Calls
      - Governance
      - Privacy Mode
      - Blockchain Inspection
      - Transaction Builder
   - Blockchain APIs  (**with examples!)
      - Database API
      - Account History API
      - Crypto API
      - Network Broadcast API
      - Network Nodes API   
   - More examples
## 7. Namespaces (** need to be here??)
   - Graphene::App
   - Graphene::Chain
   - Graphene::Wallet
## 8. Testnets
   - Public Testnet Details
   - Public Testnet Witness(Full) Nodes (block producing witness nodes) 
       - 1.Installation/Configuration of Witness
       - 2.Genesis Configuration
       - 3.Initializing Blockchain
          - Initializing the genesis bloc
          - Setup Block Production
       - 4.Connecting a CLI Wallet
       - 5.Establishing a Committee
       - 6.Web wallet 
          - (Since we need to provide a way for people to enter the network/blockchain, we need to install the web wallet into nginx.)
          - Dependencies
          - Fetching the web wallet
          - Configuration / Compilation
       - 7.Setup the Faucet      
          - Deployment tool
          - Installation of Dependencies
          - Get the Source
          - Configuration
       - 8.Setup NGing WebServer 
          - Configuration
          - Run Nginx
       - 9.Instillation of Python Library
          - Requirements   
          - Installation
        - 10.Create MPAs/UIAs
    - Private Testnet
      - 1.Prerequisites
      - 2.Folder Structure
      - 3.The Genesis Files
      - 4.Get the Blockchain ID
      - 5.Witness Configuration
      - 6.Start Block Production
      - 7.Connecting a CLI wallet


## 9. Libraries / tools
   - Python Library
      - Requirements   
      - Installation
## 10. Examples
   - Trade
   - Exchanges
   - Create MPAs/UIAs
   - more...

## 11. QA
   


