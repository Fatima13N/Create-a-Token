# Create-a-Token
This is solidity program creates, records and burn tokens.
# Description
There are Total two functions, three state variables and one mapping in the contract.
1. The State Variabels
   
     - **tokenName**: This is a `string` type variable which represents the name of token. It is made `constant` because the name does not be changed after the deployment of contract.
      
     - **tokenAbbr**: This is also a `string` type variable which represents the abbreviation of token. It is also made `constant` becouse of the same reason above.
      
     - **totalSupply**: This is a `uint256` type variable which represents the total number of token exist at anytime. The type is `uint256` becouse totalSupply can not be a negative value.

       
3. The mapping variable
   
     - **balances**: This is a mapping of `address => uint256` which keeps record of `addresses` and the `total number of token associated with each of them`.

       
5. The Functions
   
   - **mint**: This function is for adding tokens in accounts. It takes two perameters as input an `_address` (an `address` type) and `number of tokens` (an `uint256` type). It is made `external` becouse the function will only be called outside the contract. After the sucsessful execution of this function `totalSupply` value will inceresed by value of `number of tokens`, and  the balaces of given address will also be incresed by the value of `number of tokens`.
     
   - **burn**: This function is for removing a token from accounts. It is also made `external` for the same reason above. It taken two perameters as input an `_address` (an `address` type) and `number of tokens` (an `uint256` type), and a returns `bool` type variable. If the given address does not have the amount of tokens mentianed as in input, the function will retrun `false`, suggesting there is no modifiaction made in state variables. If that is not the case `totalSupply` value will decresed by value of `number of tokens`, and also the balaces of given address will also be decresed by the value of `number of tokens`, and it will return `true`.
  
# License
This project is licensed under the MIT License - see the LICENSE.md file for details
