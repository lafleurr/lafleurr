## TOKEN
Create a Token

## Description

In this project we created contract that has public variables about our coin. It has main functions such as mint and burn function. 
## Getting Started

### Executing program

To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are in the compiler. Copy and paste the following code: 



```javascript
// SPDX-License-Identifier: MIT OR GPL-3.0
// pragma solidity ^0.8.0;
contract MyToken {

    // public variables here
    string public  tokenName = "META";
    string public tokenAbbrv = "MTA";
    uint public totalSupply = 0;


    // mapping variable here
    mapping (address => uint ) public balances;

  ///solidity
// mint function
function mint (address _address, uint _value ) public  {
    totalSupply += _value;
    balances [_address] += _value;
}
///
    // burn function
    function burn (address _address, uint _value ) public  {
        if (balances[_address]>= _value ){
            totalSupply += _value;
            ///
            balances[_address] -= _value;
            ///
        }
    }
}
```
## Authors

Contributors names and contact info



## License

This project is licensed under the [NAME HERE] License - see the LICENSE.md file for details
