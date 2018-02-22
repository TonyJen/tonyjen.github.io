---
layout: post
title:  "Online Solidity Compiler "
date:   2018-02-17 00:14:52 -0500
categories: ethereum 
---

Now we will create a sample program in solidity. A good place to run your code is http://remix.ethereum.org/. It is an online editor that runs solidity with it's own blockchain so you don't have to install anything on your computer.

Here is a simple program:

```
pragma solidity ^0.4.16;
contract HelloWorld {
 
 uint256 counter = 5; //state variable we assigned earlier
 function add() public {  //increases counter by 1
  counter++;
 }
 
 function subtract() public { //decreases counter by 1
  counter--;
 }
}
```

This program will create a contract that have a counter value.

![Solidity IDE](/assets/solidity online ide.png){:class="img-responsive"}

The application created 2 functions, add and substract. Click on the button will create a block in Ethereum blockchain that changes the counter value.

Here you can check the values of counter as you click on add or substract.

Enjoy!
