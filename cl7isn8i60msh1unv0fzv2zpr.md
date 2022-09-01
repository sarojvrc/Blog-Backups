## Complete Solidity Code Deployment Process

# Solidity!

I guess many of you know, that Solidity is the programing language for Ethereum smart contract development. If you are new to solidity, don't worry, today we will be having a complete solidity code development process as well as we will see how to deploy a smart contract in solidity!

*Great Saroj :) *

### What is Solidity

Solidity is a high-level statically typed programming language. With the help of this, we can create smart contracts for uses such as voting, crowdfunding, blind auctions, and multi-signature wallets. It is mostly used for Ethereum smart contract development. Solidity is behave differently from any other programming language like Java, Javascript, C++, etc. In this article, we will see how solidity smart contracts are written and the deployment process. 

*But Saroj, where to write this solidity smart contract as you said, it behaves diff from other programming languages? Like any IDE?*

Great question! The best part is, to write solidity smart contracts we no need any application or software in our local system. We can write directly in the browser. Just hit %[https://remix.ethereum.org/] URL and Boom! You will see a workspace like the one below. 

![Remix IDE.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1662016299600/jBKp3pAkn.png align="left")

In this window, you can see some examples of smart contracts. To create a new file just click on the new file icon. 

![Remix Create file.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1662016487379/jkwsuOTMM.png align="left")

Now, let's write a solidity contract to check whether a particular age can vote or not. 

```
//SPDX-License-Identifier: GPL-3.0

//we have to mention a version no the solidity
pragma solidity >= 0.5.0 < 0.9.0;
contract IfElse{
    uint public age;

    //function to set a new age
    function setAge(uint newAge) public{
        age = newAge;
    }

    //function to check whether the age is able to vote or not
    function IsVotor() public view returns(string memory){
        string memory voter;
        if(age >= 18){
            voter = "Can Vote";
        }else{
            voter = "Can't Vote";
        }
        return voter;
    }
}
``` 
After writing the code, it will check for the compilation process. To know more about the compilation process please check my previous article [here](https://medium.com/coinmonks/smart-contract-and-its-compilation-process-34868abccb69)

During the compilation process, we have to choose one solidity compiler version. Also, make sure that the version is included in your contract code. 
![Solidity version.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1662017032737/3Zy0qZvrZ.png align="left")

Let's have an error and check what it looks like. 

![Compilation error.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1662017124281/9KkyJXuC2.png align="left")
As you can see above, I removed the semicolon in line no. 12. Solidity compiler gives an error and says, hey bro, please add a semicolon. Once we resolve all the errors, then again we have to compile. We can also set auto-compile. 

![compilation success.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1662017246594/hm2-kJvma.png align="left")
Once the compilation process gets successful, it will display a green tick mark on the left side. 

**Then only we can move to the deployment process**

Let's deploy our smart contract!

To deploy the smart contract we have to choose a Remix VM(Virtual Machine). This is a simple test smart contract, so we can choose from London or Berlin. 

![Remix env choose.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1662017697542/GtF99XGRw.png align="left")

The next step is we have to assign an Ethereum account address to run the deployment. 

![account addess choose.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1662017815515/WtranpGeN.png align="left")

As you can see we have 100 ethers in each address, those are not real ethers, these are only for testing and there are of no real value. Once we choose an address, we have to set the Gas limit, which is used for deploying the smart contract on Ethereum VM. Once we set it all, then we can click on the deploy button. And our contracts will be deployed successfully. You can see the deployed contracts below. 

![contract deployed.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1662018065286/uX3-1d7dG.png align="left")

**Now time to test our smart contract!**

Once successfully deployed we can test the smart contract. If you click the buttons it will show the default value. 

![default contract value.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1662018259576/mnq4Mnf9-.png align="left")

As you can see in the above image when I clicked the age, it is showing *0*. and it shows *Can't Vote* for the function. Now let's put some value in the *setAge* and test again. 

![age 18 contract.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1662020255199/kPdx-qYyD.png align="left")

Now we inserted 18 in the *setAge*, and if we click the *age*, now it will show 18. Also now we can see *Can Vote* after clicking the function.

This is a small overview of the deployment process of the smart contract. I know this is kind of confusing if you are new to solidity. But trust me, once you get into it, it will more fun :) I hope you all love this article and enjoyed the reading. Don't forget to try it out. 

*Thanks, Saroj, this is a great demo. waiting for your next one.*

See you soon with an awesome topic. 
















