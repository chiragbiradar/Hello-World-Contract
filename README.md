# 💻 Hello-World-Contract

## **Writing the solidity contract**

Install [node from here](https://nodejs.org/en/).

Open the terminal and run the following commands.

```
mkdir Hello-World
cd Hello-World
ls
npm init --yes
npm install --save-dev hardhat
npx hardhat
```

When you run the last command, you will get an option to create an Empty project with hardhat config. Do pick that and you will see something like this.

```
888    888                      888 888               888
888    888                      888 888               888
888    888                      888 888               888
8888888888  8888b.  888d888 .d88888 88888b.   8888b.  888888
888    888     "88b 888P"  d88" 888 888 "88b     "88b 888
888    888 .d888888 888    888  888 888  888 .d888888 888
888    888 888  888 888    Y88b 888 888  888 888  888 Y88b.
888    888 "Y888888 888     "Y88888 888  888 "Y888888  "Y888
 

The contracts directory will have all the contracts for the project and scripts directory will have all the deployments scripts and other stuff related to the project. By now the structure of your project will look something like this.

```
HelloWorld
> contracts
> node_modules
> scripts
hardhat.config.js
package-lock.json
Package.json
```

The contracts directory will have the contract of your Hello World. Create a HelloWorld.sol file in the contracts folder and write the following code.

```
/SPDX-License-Identifier: UNLICENSED
 
pragma solidity >= 0.7.3;
 
contract HelloWorld {
    //events
    //states
    //functions
 
    event messagechanged(string oldmsg, string newmsg);
 
    string public message;
 
    constructor(string memory firstmessage) {
        message = firstmessage;   
    }
 
    function update(string memory newmesssage) public {
        string memory oldmsg = message;
        message = newmesssage;
 
        emit messagechanged(oldmsg, newmesssage);
 
    }
}
```


