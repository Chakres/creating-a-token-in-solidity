# Minting and Burning Token Contract

## Description

The Solidity smart contract is a basic implementation of a custom token that follows some aspects specific standard. This contract provides functionalities for minting and burning tokens, as well as tracking balances and total supply.

## Getting Started

### Prerequisites

* Ethereum development environment (such as Remix or Truffle)
* Basic understanding of Solidity programming

### Installing

1. Download the creating_a_token.sol file.
2. Open your Ethereum development environment or an Online Compiler.

### Executing the Contract

1. Compile the Dodgecoin.sol file in your Ethereum development environment.
2. Deploy the compiled contract to an Ethereum network.
3. Interact with the contract using its functions:

#### Mint Tokens

To mint new tokens and increase the total supply and balance of an address, call the `mintSupply` function:

```solidity
function mintSupply(address _address, uint _value) public {
    totalSupply+=_value;
    balances[_address]+=_value;
}
```

#### Burn Tokens

To burn tokens and decrease the total supply and balance of an address, call the `burnSupply` function:

```solidity
function burnSupply(address _address, uint _value) public {
     if(balances[_address]>=_value)
        {
            totalSupply-=_value;
            balances[_address]-=_value;
        }
}
```

## Help

If you encounter any issues or have questions about using the contract, you can refer to Ethereum's official documentation .

## Authors

K Chakresh

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details.
