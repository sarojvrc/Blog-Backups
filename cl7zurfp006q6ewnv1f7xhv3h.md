## Deploying a Smart Contract with Truffle Ganache

# Ganache

Today we will see how we can deploy a smart contract with the help of truffle ganache. Ethereum Ganache is a local in-memory blockchain designed for development and testing. It simulates the features of a real Ethereum network, including the availability of a number of accounts funded with test Ether. Ethereum Ganache is available in two versions: a graphical application with a user interface and a command line version. To run Ganache in our system first we have to download the GUI using this [link](https://trufflesuite.com/ganache/), also we have to install the Ganache for the Ganache CLI. To install run this command. Open your terminal and type the below command. 

```
npm install -g ganache-cli
``` 

Once successfully installed, we can check the version of the truffle ganache using the below command. 

```
truffle version
``` 

we can see the below output if the installation was successful. 

```
Truffle v5.5.5 (core: 5.5.5)
Ganache v^7.0.3
Solidity v0.5.16 (solc-js)
Node v16.13.0
Web3.js v1.5.3
``` 

**Yep! we have successfully installed the truffle and ganache. Now let's set up the truffle project.** 

## Create a Truffle Project

We will create the truffle project using VS Code, if you don't have please download using this [link](https://code.visualstudio.com/download). Once downloaded and installed, open the VS Code and create a folder inside it. And on the top click on *New Terminal*.

![1_new terminal.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1663048837751/6XqUF9VF4.png align="left")

It will open a new cmd inside the vs code. Then type the command to create a new truffle project as below. 

```
truffle init
``` 

Now we can see our truffle project is created successfully. 

![2_truffle init.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1663049064871/_yx2wABnX.png align="left")

As well as you can see it also created some folders inside our vs code. 

![3_truffle project folder (2).png](https://cdn.hashnode.com/res/hashnode/image/upload/v1663049145632/YfiWswve_.png align="left")

There is a total of 3 folders named *contracts, migrations, and test*. As you can guess, you have to write all our smart contracts inside the *contracts* folder, and while deploying the migrated contracts will automatically come inside the *migrate *folder. Like this, for testing our contracts we can use the *test* folder. Also, there is a *truffle-config.json* file we can see. In this file, we have to modify depending on our deployment requirements. We will see all details in this article. 

### Ganache 

Before deploying the smart contract let's have a look at our Ganache GUI. Open your installed Ganache and start the *Ethereum Quickstart*. Once it is launched successfully you can see a home screen like below. 

![4_ganache homepage.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1663050099319/ADH8b7VtZ.png align="left")

I hope you followed my previous article where we deployed a smart contract using Remix IDE, if not follow this [link](https://medium.com/coinmonks/complete-solidity-code-deployment-process-f88be7913990). We saw how Remix IDE provided us some addresses, like this Ganache also provided us some test Ethereum addresses with containing 100 ether each. This ether has no real value, this is only for testing purposes. Also if you see in the *Blocks* tab, we can see there is only Block-0 is available. 

![5_ganache block 0.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1663050616204/pZewwXaoo.png align="left")

Once we deployed our smart contract, then only we can see the new blocks. We can explore the remaining tabs in the Ganache GUI. Now, let's deploy the smart contract. 

### Deploying the Smart Contract

As you can see we have a folder called contracts, and in this folder, a smart contract is available before. 

```
// SPDX-License-Identifier: MIT
pragma solidity >=0.4.22 <0.9.0;

contract Migrations {
  address public owner = msg.sender;
  uint public last_completed_migration;

  modifier restricted() {
    require(
      msg.sender == owner,
      "This function is restricted to the contract's owner"
    );
    _;
  }

  function setCompleted(uint completed) public restricted {
    last_completed_migration = completed;
  }
}

``` 

Hold On! Before deploying we have to modify the truffle-config.js file as we are using Ganache GUI. As you can see in the Ganache the server is 7545. Let's modify the file. Uncomment the development code and make changes as below. 

```
development: {
     host: "127.0.0.1",     // Localhost (default: none)
     port: 7545,            // Standard Ethereum port (default: none)
     network_id: "*",       // Any network (default: none)
    },
``` 

**Yep! we are all set to deploy! **

Now, open the terminal inside the vs code and run the following command. 

```
truffle migrate
``` 

If all goes well, you can see the following output below. 

```
Compiling your contracts...
===========================
> Compiling .\contracts\Migrations.sol
> Artifacts written to C:\Users\DEEL\Desktop\Ganache\build\contracts
> Compiled successfully using:
   - solc: 0.8.12+commit.f00d7308.Emscripten.clang

Starting migrations...
======================
> Network name:    'development'     
> Network id:      5777
> Block gas limit: 6721975 (0x6691b7)

1_initial_migration.js
======================

   Deploying 'Migrations'
   ----------------------
   > transaction hash:    0xb8262dcf48a0206de348870c38af3e2bfebe886840b9d99136239541a130343e
   > Blocks: 0            Seconds: 0
   > contract address:    0x6f9291645850130DBe0FC6673a2AF7441fd70B14
   > block number:        1
   > block timestamp:     1663047343
   > account:             0x8FA9410C97AbC21aEf6b12ddAB0B6cfFf6B8a4a4
   > balance:             99.99502316
   > gas used:            248842 (0x3cc0a)
   > gas price:           20 gwei
   > value sent:          0 ETH
   > total cost:          0.00497684 ETH

   > Saving migration to chain.
   > Saving artifacts
   -------------------------------------
   > Total cost:          0.00497684 ETH

Summary
=======
> Total deployments:   1
> Final cost:          0.00497684 ETH
``` 

Now if you noticed you will see, that a new file is created inside the *migrations* folder named *1_initial_migration.js*.  1 is used for the serialization of the deployment process, which means it will deploy first. 

```
const Migrations = artifacts.require("Migrations");

module.exports = function (deployer) {
  deployer.deploy(Migrations);
};

``` 

Also, we can see in the output our smart contract is deployed and we can see all these details in the Ganache GUI also. You can see the address 0x8FA deducted some ethers. 

![6_ganache balance.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1663051259083/_jMBdhWnw.png align="left")

Now, if you check in the Blocks Tab, a new block will be added. 

![7_ganache.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1663051536451/ykqWHgSbA.png align="left")

Here we can see the details of our transaction. 

![8_ganache.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1663051548287/PmHQT_szs.png align="left")

If you click one of the transactions, you can see all details for that transaction below. 

![9_ganache.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1663051645844/oTMHTtT2O.png align="left")

Here we can see the SENDER ADDRESS, CREATED CONTRACT ADDRESS, VALUE, GAS USED, GAS PRICE, GAS LIMIT, MINED IN BLOCK, and TX DATA. We have successfully deployed our smart contract with the help of truffle and ganache. Try it with yourself, I am sure you will enjoy it. 

Thanks for reading this article, see you soon with a new topic. 

