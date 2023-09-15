# Solidity Beginner(metacrafters)

This is a solidity project to create a token.

## Description

In this project we will create a token with a its name and its abbreviation and also its total supply.
After creating the token we have added some amount of values to it and also dedcuted using two functions(mint and burn).

## Getting Started

### Installing

You can run this program on any offline IDE or on Remix.

### Executing program

contract MyToken {

    // public variables here
    string public tokenName = "Goku";
    string public tokenAbbrev = "GKU";
    uint public totalSupply = 0;
    // mapping variable here
    mapping(address => uint) public balances;
    // mint function
    function mint(address _mintadr, uint _mintval)public{
        totalSupply += _mintval
        balances[_mintadr]+=_mintval;
    }
    // burn function
    function burn(address _burnadr, uint _burnval)public{
        if(balances[_burnadr] >=_burnval){
        totalSupply -= _burnval;
        balances[_burnadr]-=_burnval;
        }
    }
}
We created a token "Goku" with its abbreviation "GKU" and its total supply as 0. We then created a connection to the address and the value of the token and stored it in the balance of the token.
As you can see here we have creating two functions mint and brun.
The mint function is used to add values to a token and save it to its balance and as well ad the total supply of the token(Goku).
The burn fundtion is used to remove a certain vakue form the token's balance as well as its total supply.

## Help

When creating the burn function we have to make sure the balance of the token is more compared to the value entered to reduce.

## Authors

@dhyanms@gmail.com


## License

This project is licensed under the [MIT] License - see the LICENSE.md file for details
