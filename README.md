# Solidity Contract

This Solidity program is a simple program that demonstrates the basic syntax of making a contract in Solidity programming language. The purpose of this program is to serve as a starting point for those who are new to contracts in Solidity and want to know how to implement it.

## Description

This program is a simple contract written in Solidity, a programming language used for developing smart contracts on the Ethereum blockchain. The contract has a 2 single functions "mint" and "burn" that adds and reduce the given amount from that address.  

### Executing program

To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., MyToken.sol). Copy and paste the following code into the file:

```javascript
// SPDX-License-Identifier: MIT
pragma solidity 0.8.7;
contract MyToken {

    // public variables here
    string public token_name = "Rushan";
    string public token_abbreviation = "RG";
    uint public total_supply = 0;

    // mapping variable here
    mapping(address=>uint) public balances;

    // mint function
    function mint(address _address, uint _value) public {
        total_supply += _value;
        balances[_address] += _value;
    }
    
    // burn function
    function burn(address _address, uint _value) public {
        if ( balances[_address] >= _value ) {
            total_supply -= _value;
            balances[_address] -= _value;
        }
    }
}
```

To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.7" (or another compatible version), and then click on the "Compile MyToken.sol" button.

Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the "MyToken" contract from the dropdown menu, and then click on the "Deploy" button.

Once the contract is deployed, you can interact with it by calling the mint or burn function. Click on the "MyToken" contract in the left-hand sidebar, and then click on the "mint" function , add address and a value to it then click on "burn" function and add a value to it. Click on "transact" . Now you can check your balance by clicking on "total_supply"


## Authors

Rushan 
[@metacraftersio](https://twitter.com/metacraftersio)


## License

This project is licensed under the MIT License - see the LICENSE.md file for details
