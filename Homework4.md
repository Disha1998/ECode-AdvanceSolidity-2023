#### Optimising Storage
**Question: Take this contract Use the sol2uml tool to find out how many storage slots it is using. By re ordering the variables, can you reduce the number of storage slots needed ?**

**What I did,**

**What is sol2uml? => Sol2UML ek tool hai jo Solidity contracts se UML diagrams banane me madad karta hai. Yeh diagrams aapko contract ki structure aur interactions ko visual tarike se samajhne mein madad karti hai. Sol2UML ka use karne ke liye neeche diye gaye kadam follow karein:**

**Steps for how you can use sol2uml to create a class diagram for your contract:**

1)Install

```
npm install -g sol2uml
```

2) Save your contract code to a .sol file. In your device/folder,


```
// SPDX-License-Identifier: UNLICENSED
pragma solidity ^0.8.13;

contract Store {

    struct payments {
        bool valid;
        uint256 amount;
        address sender;
        uint8 paymentType;
        uint256 finalAmount;
        address receiver;
        uint256 initialAmount;
        bool checked;
    }
    uint8 index;
    uint256 public number;
    bool flag1;
    address admin;
    mapping (address=>uint256) balances;
    bool flag2;
    address admin2;
    bool flag3;
    payments[8] topPayments;


    constructor(){

    }


    function setNumber(uint256 newNumber) public {
        number = newNumber;
    }

    function increment() public {
        number++;
    }
}

```

3)Run sol2uml to generate the class diagram:

```
sol2uml  Store.sol
```

After that sol2uml will generate a UML diagram in SVG format by default. 
### ex: file:///Users/jaydippatel/classDiagram.svg

   ![Screenshot 2023-10-14 at 10 30 17 PM](https://github.com/Disha1998/ECode-AdvanceSolidity-2023/assets/69969675/ad638459-a152-4aa9-9d38-6cc921276338)

––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––

### Foundry Introduction

**install** 

```
npm i foundry
```

#### https://www.npmjs.com/package/foundry

First run the command below to get foundryup , the Foundry toolchain installer: curl -L https://foundry.paradigm.xyz | bash If you do not want to use the redirect, feel free to manually download the foundryup installation script from here. Then, run foundryup in a new terminal session or after reloading your PATH . Other ways to use foundryup , and other documentation, can be found here https://github.com/foundry-rs/foundry/tree/master/foundryup.

––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––



### Try out the Solidity Template or the Foundry Template


![Screenshot 2023-10-14 at 11 19 45 PM](https://github.com/Disha1998/ECode-AdvanceSolidity-2023/assets/69969675/b4b67d66-6928-4782-963c-0c9f3bb66cb0)


```
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.9;

contract MyCon{
    function a(
    function(
        function(
            function(
                function(
                    function() external pure
                )external pure
            )external pure
        )external pure
    ) external pure
 )external pure {}
}
```

**The provided code is technically valid in terms of Solidity's syntax, so it won't cause a compilation error. However, it's not written in a way that's easy to understand or practical for real-world use.**

–––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––

**Try out the Solidity Template or the Foundry Template**

**=> Tried Out Hardhat template and Foundry**

