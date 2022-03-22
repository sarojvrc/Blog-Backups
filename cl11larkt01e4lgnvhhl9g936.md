## Structure of the Block inside a Blockchain Network

**Hey Guys**, 

What's up? 

**So**, today we will see, *the structure of the block* inside a *blockchain *network. 

Let's start!

wait, wait...

Before starting, I guess you are familiar with *Blockchain*, if not, then please read my previous article [here](https://saroj.hashnode.dev/how-does-the-blockchain-work). 

Will it work for you? 

Awesome! 

Then why wait? let's start :)

As you know, *blockchain *is consists of a chain of *blocks*, it is must necessary to have some data inside a *block*. Without any data, it is impossible to insert a new *block*. Data are like oxygen for humans; without oxygen, humans can't live. Like this way, without data, *blocks *inside a *blockchain *network can't exist(*It must have some data*). 

I can't relate to a better example for this. Just kidding. :)

Cool!

**Now, let's see the *structure of a block*!**


![Blockchain Block structure.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1647880712660/QWrF8JFi4.png)

As you can see in the above diagram, a *block *is differentiated into 2 parts.

1. Block Head
2. Block Body

Let's talk about ***Block head*** first. 
![Block head.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1647883650200/htLWNYPGA.png)

*Block head* is also divided into six components. Those are
- Version number
- Previous block hash
- Merkle tree root hash
- Nbits
- Nonce
- Timestamp

![block version.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1647884816264/dO4YVrVoY.png)
The *block version* number indicates which set of *block *validation rules to follow. This is useful for a miner, who wants to mine(*to insert a new block*) inside the *blockchain *network. That means, let's say I want to mine, I need the *block version* to check the rules and regulations provided by that version. Every *block version* has some rules to follow, which is provided by the blockchain network.

![markle tree.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1647885031885/HSkxdV_qa.png)
A *Markle tree* encodes the *blockchain *data in an efficient and secure manner. It enables the quick verification of the *blockchain *data. 

![markle tree diagram.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1647920055238/auzhsvHYX.png)
The data itself is first hashed. Then the hashes are hashed again and merged. Finally, the *Merkle tree* merged into a single hash, called *root hash*. It is also called the root of the tree. 

![previous block.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1647885285591/v-b2KNVKT.png)
The hash of the previous *block *is the chain of *blockchain*. Because the hash of the previous *block *is contained on a hash of the new *block*. The blocks of the *blockchain *are all built on each other. 


![n bits.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1647885611497/WJqKwIYnj.png)
With the help of n Bits, the current difficulty is used to create this *block*. This means it will decide how the *block *is to be going to create. 


![nonce.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1647885886214/9KPQu90_m.png)
A *nonce *is a variable increment by the Proof-of-Work[(PoW)](https://www.investopedia.com/terms/p/proof-work.asp). In this way, the miner guesses a valid hash, a hash that is smaller than the target. 


![time stamp.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1647886076630/iH7vuHB0C.png)
And *timestamp *is the *block *itself. Each *block *contains a unique timestamp. A *timestamp *is accepted as valid if it is greater than the median of the previous 11 *blocks *and less than the network adjusted time. Network adjusted time is the median of all *blocks *present inside the *blockchain *network.  

Now, let's talk about the **Block body**. 

![block body.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1647886557576/-WX3KeG-n.png)
The *transaction counter* is the place where all transactions are done. Let's say, there are 10 transactions is done inside a block, then *transaction counter* creates a copy of every single transaction for its future reference. And those transactions are stored separately. 

Here, we ended up with the *structure of a block* inside a *blockchain *network. I know, it's kind of confusing, if you are new to *blockchain*. But I'm pretty sure, you must have got some idea about the *block*. 

Right? 

Awesome!

If you further need any help, try to connect with me. I'll be happy to solve your doubts. 

Till then, keep learning and keep smiling :)

Thanks for reading this. See you soon with a new article. 


[LinkedIn](https://www.linkedin.com/in/sarojvrc/) [Twitter](https://twitter.com/iamsarojb) 


