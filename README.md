# ETH_Proof_Beginner
Summer Training with Metacrafters for Learning Blockchain with Ethereum using Solidity.

# Project Title

Token Simulation: Minting and Burning

## Description

This is a basic project that simulates creating smart contracts on a local machine using the Remix IDE and the Solidity programming language for token transactions in a blockchain. The project shows how to make a simple token contract that has the ability to mint (make new tokens) and burn (destroy old tokens).

This project is a fundamental illustration of how to use Solidity to create a token on the Ethereum network. The contract maintains track of the token balances for every address and has the ability to manufacture and burn tokens. The contract makes it simple to interact with and verify token balances and details by using public variables and mappings.

## Getting Started

### Installing

* To run the project code, you need an IDE where you can run the Solidity language. One such IDE is the online Remix IDE (https://remix.ethereum.org/), which you can run on any browser of your choice.
* The code in this project can be used by simply copying it to the editor of any IDE where you can run Solidity version 0.8.7.

### Executing program

* How to run the program:
1. Copy the Solidity code provided in the "Final_Assessment" file.
2. Open Remix IDE (https://remix.ethereum.org/).
3. In the Remix IDE, create a new file and paste the copied code into it.
4. Compile the Code by either pressing "Ctrl + S" to compile the code or using the Compile button in the Remix IDE interface.
5. Use the Deploy button in the Remix IDE to deploy the contract to a local Ethereum network or a test network.
6. Use the deployed contract's interface in Remix IDE to call the mint and burn functions with appropriate parameters.
.


```solidity
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.7;

contract MyToken {

    // public variables here
    string public TokenName = "The_Name";
    string public TokenAbbrv = "The_Abbrv";
    uint public T_Supply = 0;

    // mapping variable here
    mapping(address => uint) public balances;

    // mint function
    function mint (address _address, uint _value ) public {
        T_Supply += _value;
        balances[_address] += _value;
    }

    // burn function
    function burnToHell (address _address, uint _value) public {
        if(balances[_address] >= _value){
            T_Supply -= _value;
            balances[_address] -= _value;
        }
    }
}
```

## Help

If you encounter any issues or have any questions, here are some common solutions:

1. Ensure you are using Solidity version 0.8.7 or later.
2. Check the Remix IDE console for error messages and follow the guidance provided.
3. Make sure the address you are using for minting and burning tokens has sufficient permissions and balance.

## Authors

Contributors names and contact info

Harshveer Singh    
mail: harshveerraka@gmail.com


## License

This project is licensed under the [MIT] License - see the LICENSE.md file for details
