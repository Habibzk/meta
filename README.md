# Final Assesment Project - Meta 

this final assesment code is the project to the final challenge of the metacrafter's beginner solidity course.

## Description

This is code for a token name "Earth Token" that has a mapping to addresses that mint the token and a corresponding burn function to account for the subtraction of tokens in that same address.

## Getting Started

### Installing

* To use this code all you have to do is copy/paste in remix and deploy to access functions

### Executing program

* Once deployed the code has 2 setter functions and 4 getter functions

* The 2 setters
``` Solidity
    // mint function
    function mint (address _address, uint _value) public {
        totalSupply += _value;
        balances[_address] += _value;
    }
```

``` Solidity
    // burn function
    function burn (address _address, uint _value) public {
        if (balances[_address] >= _value)
        {totalSupply -= _value;
        balances[_address] -= _value;}
    }
```

* code that initalizes the 4 getter functions

```
    // public variables here
    string public tokenName = "Earth Coin";
    string public tokenAbbrv = "ERH";
    uint public totalSupply = 0;
```

```
    // mapping variable here
    mapping(address => uint) public balances;

```

## Help

Adjust gas limit to test viability of different options

## Authors

Habib "Zk" Salami

## License

This project is licensed under the MIT License - see the LICENSE.md file for details




