ContractMyToken
ContractMyToken is a Solidity smart contract that represents a simple token contract. This contract allows for the creation, minting, and burning of tokens.

Features
Token Name: The contract stores the name of the token as a string in the tokenName variable.
Token Abbreviation: The contract stores the abbreviation of the token as a string in the tokenAbbrv variable.
Total Supply: The contract keeps track of the total supply of tokens in the totalSupply variable.
Balances: The contract uses a mapping named balances to track the token balance of each address.
Deployment
The contract is deployed using Solidity version 0.8.0 or a compatible version.

Functions
Constructor
The contract constructor is called when the contract is deployed. It takes three parameters: _tokenName, _tokenAbbrv, and _totalSupply. These parameters initialize the token's name, abbreviation, and total supply, respectively. The total supply is assigned to the deploying address.

mint
The mint function allows for the creation of additional tokens. It takes two parameters: _to (address) and _value (uint). The function increases the total supply by _value and adds the corresponding amount to the balance of the provided address _to.

burn
The burn function allows for the removal of tokens from a specific address. It takes two parameters: _from (address) and _value (uint). The function verifies that the _from address has a sufficient balance to burn the specified _value of tokens. If the balance is sufficient, the total supply is reduced by _value, and the _from address balance is decreased accordingly.
