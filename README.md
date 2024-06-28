# Cute Kitten Token Smart Contract
This contract is written in Solidity, a programming language specifically designed for building smart contracts on the Ethereum blockchain.
# Description
It is a basic implementation of an ERC-20-like token on the Ethereum blockchain using Solidity. This smart contract allows for the minting and burning of tokens, and it keeps track of the total supply and individual balances. This sample smart contract demonstrates the basic functionalities of creating and managing a token on the blockchain. With these functions, we can mint new Kitty coins, distribute them to users, and even allow users to burn their Kitties if they choose.
## Getting Started
## Executing program
To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., HelloWorld.sol). Copy and paste the following code into the file:



solidity
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.18;
contract Cute_Kitty_Token {
    // public variables here
    string public TokenName = "Cute Kittens";
    string public TokenAbbrv = "Kitty";
    uint public TokenSupplyqty = 0;
    // mapping variable here
    mapping (address => uint) public balances;
    // mint function
    function mint (address _address,uint amount) public {
        TokenSupplyqty += amount;
        balances[_address] += amount;
    }
    // burn function
        function burn (address _address,uint amount) public {
            if (balances[_address] >= amount){
            TokenSupplyqty -= amount;
            balances[_address] -= amount;
            }
        }
}


To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.18" (or another compatible version), and then click on the "Compile HelloWorld.sol" button.

Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the "HelloWorld" contract from the dropdown menu, and then click on the "Deploy" button.

Once the contract is deployed, you can interact with it by calling the minting and burning function. Click on the "Cute_Kitten_Token"  contract in the left-hand side bar, and then click on the Mint function, call the mint function with the recipient's address and the number of tokens to mint, and then click on the Burn function after that click on the "transact" button to execute the function. Then,  call the burn function with the address to burn from and the number of tokens to burn then again click on the "transact" button to execute the function and retrieve the balance of the given address. 
## License
This project is licensed under the MIT License.
## Acknowledgments
- Inspired by the ERC-20 token standard.
- Developed using Solidity and Ethereum tools.

Feel free to reach out for any questions or further improvements to this project.
