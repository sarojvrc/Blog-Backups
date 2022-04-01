## What does a Block look like in a Blockchain?

**Hey Guys,** 

Hope all are doing well. 

Great!

**Today we will see about the *block*, and what does it look like in a blockchain network. **

I assume you are aware of the *block *structure. If not, please read my previous article [here](https://medium.com/coinmonks/structure-of-the-block-inside-a-blockchain-network-7ad66ea5bea).

**Awesome**. 

Let's start then. :)

*Block *is the head of a blockchain network. without blocks, you can't create a blockchain. and every *block *interlinked with each other. Let's see how.


![Block 2.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1648774977289/6VPl_6kYv.png)

As you can see in the above diagram, a *block *is consists of **Nonce**, **SHA256**, **the previous block signature**, and **some transactions**. 

**Genesis Block**

The very first *block *is called a *Genesis Block* or *Block 0*. Because this *block *doesn't contain any previous block signature. 

Able to understand somewhat? 

Great!

Let's see other parts.

**Nonce**

Every *block *must have a *Nonce*. A *nonce *is created by a miner, who mines the *block *into a blockchain network. These are generated in a particular way through the mining algorithm. It contains some value, and it is different from other *nonce *values. 

**SHA256**

*SHA256 *is a simple hash algorithm that crunches any length of data into a unique string of a fixed length. Each *block *has a different *HSA256*. 

Eg. ba7816bf8f01cfea414140de5dae2223b00361a396177a9cb410ff61f20015ad

**Signature **

Genesis block doesn't contain a *signature*. Because, it is the very *first block*, or *block 0*. Once the genesis *block *is formed, the *signature *will be added to the next *block*. A *signature *is the HSA256 value of the previous *block*. Block 1's *signature *value is the same as Block 0's SHA256 value. Block 2's *signature *value is the same as Block 1's SHA256 value. And so on. With the help of this *signature *value, every *block *is linked with another *block*. 



**Transactions**

Each *block *contains some transactions, but not the genesis *block*. *Transactions *can be anything like let's say, A has 10 coins, B has 20 coins and C has 40 coins. A transferred 5 coins to B and C transferred 10 coins to B. Like this, every *transaction *is stored in a *block*. 

I think you have got some idea about the block. 

**Great!**

If you further need any help, try to connect with me. I’ll be happy to solve your doubts.

Till then, keep learning and keep smiling :)

Thanks for reading this. See you soon with a new article.

[LinkedIn](https://www.linkedin.com/in/sarojvrc/)   [Twitter](https://twitter.com/iamsarojb)



