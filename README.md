# CREATING A NEW TOKEN

In this project we are going to create a new Tokens , by adding different function like mint and burn. This project is going to allows for the creation and deletion of token .

## Description

This project is going to related with the blockchain which is highly boomed nowadays , we are going to use solidity in this project so that we can create a code such that it can create a various new token . It include various functions , loops , conditional statement etc. 

## Getting Started 

### Executing Program

Online Code Editor: REMIX IDE (It is an online software to execute various coding language like solidity blockchain).

// SPDX-License-Identifier: MIT
pragma solidity 0.8.26;

contract MyTokenFun{

    string public token_Name="AMAN";
    string public token_Abbv="KR";
    uint public total_Supply=0;

    mapping(address => uint) public balances;

    function mint(address accountAddress,uint amount ) public {
        total_Supply += amount;
        balances[accountAddress] += amount;
    }

function burn(address accountAddress,uint amount) public  {

    if(balances[accountAddress]>=amount){ 
        total_Supply -= amount;
        balances[accountAddress] -= amount;
    }
}
}
