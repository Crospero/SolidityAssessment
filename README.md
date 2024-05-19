# My Token

MyToken is a simple Solidity smart contract that facilitates the creation, distribution, and destruction of a custom cryptocurrency token. It provides basic functionality for minting new tokens and burning existing ones.

## Description

The MyToken project presents a foundational smart contract written in Solidity, designed to enable the creation, distribution, and controlled destruction of a custom cryptocurrency token on the Ethereum blockchain. With a clear and concise structure, the contract encapsulates essential functionalities, including token creation, balance management, and token burning.

## Getting Started

### Executing program

To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., MyToken.sol). Copy and paste the following code into the file:
```
pragma solidity 0.8.18;

contract MyToken {

    // public variables here
    string public tokenName = "Goldeen";
    string public tokenAbbrv = "GDN";
    uint public totalSupply = 0;

    // mapping variable here
    mapping(address => uint) public balances;

    // mint function
    function mint (address _address, uint _value) public {
        totalSupply += _value;
        balances[_address] += _value;
    }

    // burn function
    function burn (address _address, uint _value) public {
        if (balances[_address] >= _value) {
            totalSupply -= _value;
            balances[_address] -= _value;
        }
    }
}
```
To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.18" (or another compatible version), and then click on the "Compile MyToken.sol" button.

Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the "MyToken" contract from the dropdown menu, and then click on the "Deploy" button.

Once the contract is deployed, you can interact with it by calling the Mint and Burn functions. Click on the "MyToken" contract in the left-hand sidebar, and then click on the "Mint" and "Burn" functions. Finally, click on the "transact" button to execute the function and retrieve the desired results.

## Authors

National Teachers College Crospero

422000749@ntc.edu.ph


## License

This project is licensed under the MIT License - see the LICENSE.md file for details
