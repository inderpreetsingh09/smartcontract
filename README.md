SafeBank Smart Contract
Overview
SafeBank is a simple Ethereum smart contract that demonstrates the usage of the require(), assert(), and revert() statements in Solidity. This contract allows users to deposit and withdraw funds, check their balances, and for the owner to manage the contract and perform emergency withdrawals.

Purpose
The primary purpose of this project is to provide a clear example of how to use key error handling and validation functions (require(), assert(), and revert()) in Solidity. By implementing basic banking functionality, the contract showcases practical use cases for these statements, helping developers understand their differences and appropriate usage.

Functionality
Deposit Funds:

Users can deposit Ether into the contract.
Uses require() to ensure the deposit amount is greater than zero.
Withdraw Funds:

Users can withdraw their deposited Ether.
Uses require() to ensure the withdrawal amount is greater than zero and that the user has sufficient balance.
Uses require() to ensure the transfer is successful.
Set a New Owner:

The current owner can set a new owner for the contract.
Uses require() to ensure the new owner address is valid.
Restricted to the current owner using the onlyOwner modifier.
Check Balance:

Users can check their deposited balance.
Check Invariant:

Demonstrates the use of assert() to ensure internal consistency by checking if the total balance of the contract equals the sum of individual user balances.
Emergency Withdraw:

The owner can withdraw all Ether from the contract in case of an emergency.
Uses revert() to stop the transaction if the contract balance is less than 1 Ether.
Uses require() to ensure the transfer is successful.
Restricted to the owner using the onlyOwner modifier.
Usage
To use this contract, you will need to deploy it to the Ethereum blockchain using a development environment such as Remix, Truffle, or Hardhat. Below are the basic steps to deploy and interact with the contract using Remix:
