# Cute-Kitten Smart Contract Solidity Project for Metacrafters assessment
This Solidity contract creates a fun token called "Cute Kittens" that can be minted and burned.

# Requirements fulfilled in this project
1. This contract has public variables that store the details about a coin (Token Name, Token Abbrv., Total Supply)
2. This contract will have a mapping of addresses to balances (address => uint)
3. This has a mint function that takes two parameters: an address and a value. The function then increases the total supply by that number and increases the balance of the “sender” address by that amount
4. This contract will have a burn function, which works the opposite of the mint function, as it will destroy tokens. It will take an address and value just like the mint functions. It will then deduct the value 
   from the total supply and from the balance of the “sender”.
5. Lastly, this burn function should have conditionals to make sure the balance of the "sender" is greater than or equal to the amount that is supposed to be burned.
