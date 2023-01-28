# How to create an NFT in Solidity? With Example!

**Well**, finally today we will see, how we can create a simple NFT using the Solidity programming language. And, we will also see, how we can deploy the NFT.

*Excited? Me too :)*

Before moving forward I assume you are aware of NFT, and how it works, if not, please check out my article about [*this*](https://medium.com/coinmonks/what-is-nft-and-how-it-be-useful-in-the-coming-future-8a0002f3f7f)*. Great!*

To create an NFT (*Non-Fungible Token*) with a blockchain, you will need to use a programming language to interact with the blockchain’s API or *Application Programming Interface.* The exact steps and code you need to use will depend on the specific blockchain you are using, as different blockchains have their own unique APIs. In this article, we will use Solidity as a programming language with the Ethereum blockchain!

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1674880631644/3e8e244d-299d-4dc1-8dc1-096f75aa4f92.jpeg align="center")

NFT is nothing but a smart contract written in Solidity. Let's see all steps to create.

1. First, we will need to set up a development environment with the tools necessary to build and deploy smart contracts on the Ethereum blockchain. This will typically involve installing a local blockchain client (*such as Ganache*) and a Solidity compiler (*such as Remix*).
    
2. Next, we will need to define the properties of your NFT in a Solidity contract. This will include a unique identifier for the NFT, as well as any additional metadata or data you want to include in the NFT.
    

*Cool, Now let us see these steps with an example!*

```solidity
pragma solidity ^0.6.0;

import "https://github.com/OpenZeppelin/openzeppelin-solidity/contracts/token/ERC721/SafeERC721.sol";

// Contract that represents a collectible item
contract Collectible is SafeERC721 {
  // Unique identifier for the collectible
  uint256 public collectibleId;
  // Additional metadata for the collectible
  string public name;
  string public description;
  string public imageUrl;

constructor(uint256 _collectibleId, string memory _name, string memory _description, string memory _imageUrl) public {
    collectibleId = _collectibleId;
    name = _name;
    description = _description;
    imageUrl = _imageUrl;
  }
}
```

After defining our NFT contract, we will need to compile it using a Solidity compiler. It will produce a bytecode version of your contract which can be deployed to the Ethereum blockchain later.

# **How we can deploy it?**

To deploy our NFT contract to the Ethereum blockchain, we will need to use a tool like Remix or Truffle to send a transaction to the blockchain with the bytecode for your contract. It will create a new contract on the blockchain which represents our NFT.

Once our NFT contract is deployed, w can use it to create new NFTs by calling the contract’s “*mint*” function and passing in the necessary data for each NFT.

*let's see this also in coding.*

```solidity
// we need to connect to the Ethereum blockchain (rinkeby)
Web3 web3 = new Web3("https://rinkeby.infura.io/v3/YOUR-API-KEY");

// then we have to load our NFT contract
Collectible contract = Collectible.load(OUR_CONTRACT_ADDRESS, web3, CREDENTIALS);

// finally, we can create our NFT
contract.mint(1, "Collectible #1", "This is the first collectible", "https://example.com/collectible1.png");
```

*Yeah, we successfully created and deployed our simple NFT using Solidity with the Ethereum blockchain.*

It is just a basic example of how we can create an NFT with the Ethereum blockchain using Solidity. There are many other considerations and steps to be aware of when working with real NFTs and blockchains.

I hope you guys love reading this and got some idea about how we can create and deploy an NFT. In the coming future, I will come up with an article like this. Stay tuned!

*Thanks for reading :)*

Let's connect on [***LinkedIn***](https://www.linkedin.com/in/sarojvrc/) [***Twitter***](https://twitter.com/iamsarojb)