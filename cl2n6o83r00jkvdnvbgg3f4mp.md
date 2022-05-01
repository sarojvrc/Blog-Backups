## Public and Private Keys in Cryptocurrency

**Well, **

**Today, we are going to discuss public and private key, and how it is a very crucial part of cryptocurrency. **

Cool!

You all know what is a key right? In our daily life, we are using it for locking purposes, let's say, you have a key for your luggage, or you may have a key for your bag, etc. Like this, we will use this key in cryptocurrencies. 

**Let's see how :)**

You may have heard that bitcoin is based on *cryptography*, which is a branch of mathematics used extensively in computer security. Cryptography means *"secret writing"* in Greek, but the science of cryptography is more than just secret writing. 

Ownership of bitcoin is established through digital keys, bitcoin addresses, and digital signatures. 
The digital keys are not actually stored in the network but are instead created and stored by users in a file, or simple database called a *wallet*. Keys enable many of the interesting properties of bitcoin, including decentralized trust and control, ownership, and a cryptographic-proof security model. 

**So, here keys come into the picture. let's explore them. **

### Private Key 

A private key is simply a number, picked at random. Ownership and control over the private key is the root of user control over all funds associated with the corresponding bitcoin address. The private key is used to create signatures that are required to spend bitcoin you providing ownership of funds used in a transaction. The private key must remain secret at all times because revealing it to third parties is the same as giving them control over the bitcoins secured by that key. 


![private key.jpg](https://cdn.hashnode.com/res/hashnode/image/upload/v1651401579338/TsSGxkVcN.jpg align="left")

You can pick your private keys randomly using just a coin, pencil, and paper: toss a coin 256 times and you have the binary digits of a random private key you can use in a bitcoin wallet. The public key can then be generated from the private key. 

**Example:** 1E99423A4ED27608A15A261A2B0E9E52CED330AC530EDEC322C8FFC6A32S5EFYYCD0DD

### Public Key 

The public key is calculated from the private key using elliptic curve multiplication, which is irreversible: K = k*G, where k is the private key, G is a constant point called the generator point, and K is the resulting public key. We can generate multiple public keys from a private key, but it is impossible to generate the private key, from a public key. 


![elliptic-curve-250px.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1651402053677/94srLZ6ZR.png align="left")

*Elliptic curve multiplication* is a type of function that cryptographers call a *"trap door"* function: it is easy to do in one direction and impossible to do in the reverse direction. The owner of the private key can easily create the public key and then share it with the world knowing that no one can reverse the function and calculate the private key from the public key. This mathematics trick becomes the basis of an unforgettable and secure digital signature that proves ownership of bitcoin funds. 

This is the basic idea about **public and private keys**. I am sure you got some idea of how these work inside a cryptocurrency. 

**That's all for today. **

**See you soon with a new article!**

