## Smart Contract and its Compilation Process

# Smart Contract!

Before starting the smart contract I hope all of you know about the simple contract. Right? 

## What is a Contract?

A contract is a written or spoken agreement, especially one concerning employment, sales, or tenancy, that is intended to be enforceable by law. In simple terms, it is a piece of paper where two parties make a contract that includes mutual assent and is enforceable by law. 

Like this, we can make a contract with the help of a coding language(mostly solidity), which calls a smart contract. Or we can say a smart contract is a self-executing contract with the terms of the agreement between buyer and seller being directly written into lines of code. It is simply a program that runs on the Ethereum blockchain. It's a collection of code (its functions) and data (its state) that resides at a specific address on the Ethereum blockchain.

*Ohh, Ok Saroj. That's a great feature. But wait, how to write them? *

## How to write a smart contract? 

As you all know, to write a smart contract we need a coding language. And for that, we need an IDE where we can write our smart contract. As of now, Remix IDE is the favorite tool where we can write them. It is an open-source IDE. With the help of Remix, we can develop, deploy, and we can also administer our smart contracts. 

Solidity is the most popular language to write smart contracts. In Remix, not only in Solidity but also with Vyper we can write smart contracts. 

*Interesting right? *
*Yep, Saroj :) Can you please show a smart contract what it looks like? *

Here I am writing a simple smart contract where I can store a number and I can retrieve that stored number. 

```
// SPDX-License-Identifier: GPL-3.0

pragma solidity >=0.7.0 <0.9.0;

contract Storage {

    uint256 number;

    function store(uint256 num) public {
        number = num;
    }

    function retrieve() public view returns (uint256){
        return number;
    }
}
``` 
As you can see above it is a simple smart contract. Let's try to understand all of the lines. 
In the very first line, we have to mention the license number. 

```// SPDX-License-Identifier: GPL-3.0
``` 

Then we have to mention a version number of solidity language. Also, we need to provide a contract name, in our case, it is *Storage*. Inside the storage contract, I am taking one *unit256* type variable called *number*.  And I make 2 functions named *store* and *retrieve*. 

Cool. This is a simple smart contract program that takes one number and it will store that number with the help of the *store* function. And we can retrieve that stored number with the help of the *retrieve* function. 

*Well, this is fine Saroj. But how a smart contract compiles the code? *

## Compilation of a Smart Contract


![Smart Contract.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1661364472629/faXB28R-_.png align="left")

When we compile a smart contract, it goes to the solidity compiler. Then the compiler checks all the lines for any errors. If the compilation process works fine, then it divides the smart contract into 2 parts. 


1. ABI
2. Byte Code

**1. ABI**

ABI or Application Binary Interface is the Interface or we can say, it acts like a bridge between application and smart contract. If another smart contract or application wants to access our smart contract, then they must need the ABI. Let's see what it looks like. 

> [
	{
		"inputs": [],
		"name": "retrieve",
		"outputs": [
			{
				"internalType": "uint256",
				"name": "",
				"type": "uint256"
			}
		],
		"stateMutability": "view",
		"type": "function"
	},
	{
		"inputs": [
			{
				"internalType": "uint256",
				"name": "num",
				"type": "uint256"
			}
		],
		"name": "store",
		"outputs": [],
		"stateMutability": "nonpayable",
		"type": "function"
	}
]

It is the ABI for the *Storage* smart contract. With the help of ABI, we can easily understand the structure of the smart contract. 


**2. Byte Code**

Byte code is also generated from our smart contract at the time of compilation. It is helpful while the deployment of the smart contract in the blockchain network. Without Byte code we can not deploy a smart contract in the blockchain network. 

> {
	"generatedSources": [],
	"linkReferences": {},
	"object": "608060405234801561001057600080fd5b5061012f806100206000396000f3fe6080604052348015600f57600080fd5b506004361060325760003560e01c80632e64cec11460375780636057361d146051575b600080fd5b603d6069565b6040516048919060c2565b60405180910390f35b6067600480360381019060639190608f565b6072565b005b60008054905090565b8060008190555050565b60008135905060898160e5565b92915050565b60006020828403121560a057600080fd5b600060ac84828501607c565b91505092915050565b60bc8160db565b82525050565b600060208201905060d5600083018460b5565b92915050565b6000819050919050565b60ec8160db565b811460f657600080fd5b5056fea264697066735822122023b549bd0c8231da07c9c7975eb66a2138eadd598892f1edfba57dd359ed082264736f6c63430008030033",
	"opcodes": "PUSH1 0x80 PUSH1 0x40 MSTORE CALLVALUE DUP1 ISZERO PUSH2 0x10 JUMPI PUSH1 0x0 DUP1 REVERT JUMPDEST POP PUSH2 0x12F DUP1 PUSH2 0x20 PUSH1 0x0 CODECOPY PUSH1 0x0 RETURN INVALID PUSH1 0x80 PUSH1 0x40 MSTORE CALLVALUE DUP1 ISZERO PUSH1 0xF JUMPI PUSH1 0x0 DUP1 REVERT JUMPDEST POP PUSH1 0x4 CALLDATASIZE LT PUSH1 0x32 JUMPI PUSH1 0x0 CALLDATALOAD PUSH1 0xE0 SHR DUP1 PUSH4 0x2E64CEC1 EQ PUSH1 0x37 JUMPI DUP1 PUSH4 0x6057361D EQ PUSH1 0x51 JUMPI JUMPDEST PUSH1 0x0 DUP1 REVERT JUMPDEST PUSH1 0x3D PUSH1 0x69 JUMP JUMPDEST PUSH1 0x40 MLOAD PUSH1 0x48 SWAP2 SWAP1 PUSH1 0xC2 JUMP JUMPDEST PUSH1 0x40 MLOAD DUP1 SWAP2 SUB SWAP1 RETURN JUMPDEST PUSH1 0x67 PUSH1 0x4 DUP1 CALLDATASIZE SUB DUP2 ADD SWAP1 PUSH1 0x63 SWAP2 SWAP1 PUSH1 0x8F JUMP JUMPDEST PUSH1 0x72 JUMP JUMPDEST STOP JUMPDEST PUSH1 0x0 DUP1 SLOAD SWAP1 POP SWAP1 JUMP JUMPDEST DUP1 PUSH1 0x0 DUP2 SWAP1 SSTORE POP POP JUMP JUMPDEST PUSH1 0x0 DUP2 CALLDATALOAD SWAP1 POP PUSH1 0x89 DUP2 PUSH1 0xE5 JUMP JUMPDEST SWAP3 SWAP2 POP POP JUMP JUMPDEST PUSH1 0x0 PUSH1 0x20 DUP3 DUP5 SUB SLT ISZERO PUSH1 0xA0 JUMPI PUSH1 0x0 DUP1 REVERT JUMPDEST PUSH1 0x0 PUSH1 0xAC DUP5 DUP3 DUP6 ADD PUSH1 0x7C JUMP JUMPDEST SWAP2 POP POP SWAP3 SWAP2 POP POP JUMP JUMPDEST PUSH1 0xBC DUP2 PUSH1 0xDB JUMP JUMPDEST DUP3 MSTORE POP POP JUMP JUMPDEST PUSH1 0x0 PUSH1 0x20 DUP3 ADD SWAP1 POP PUSH1 0xD5 PUSH1 0x0 DUP4 ADD DUP5 PUSH1 0xB5 JUMP JUMPDEST SWAP3 SWAP2 POP POP JUMP JUMPDEST PUSH1 0x0 DUP2 SWAP1 POP SWAP2 SWAP1 POP JUMP JUMPDEST PUSH1 0xEC DUP2 PUSH1 0xDB JUMP JUMPDEST DUP2 EQ PUSH1 0xF6 JUMPI PUSH1 0x0 DUP1 REVERT JUMPDEST POP JUMP INVALID LOG2 PUSH5 0x6970667358 0x22 SLT KECCAK256 0x23 0xB5 0x49 0xBD 0xC DUP3 BALANCE 0xDA SMOD 0xC9 0xC7 SWAP8 0x5E 0xB6 PUSH11 0x2138EADD598892F1EDFBA5 PUSH30 0xD359ED082264736F6C634300080300330000000000000000000000000000 ",
	"sourceMap": "141:356:0:-:0;;;;;;;;;;;;;;;;;;;"
}

Above is the Byte code for the same *Storage* smart contract. Byte code mainly consists of *object* and *opcodes*. object is the binary form of the smart contract where opcodes acts as an instruction to the smart object. 

*Ohh! now we are able to understand the smart contract, thanks Saroj!*

This is a simple overview of the smart contract and it's compilation process. I hope you found it informative and you enjoyed it. 

Thanks for the read. See you soon :)






