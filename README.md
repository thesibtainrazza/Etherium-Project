# MyToken Smart Contract

## Simple overview of use/purpose

This Solidity-based smart contract implements a basic ERC-20 token with mint and burn functionalities. The contract includes public variables to store token details, mappings for address balances, and functions to mint and burn tokens.

## Description

MyToken is a simple ERC-20 compatible token contract written in Solidity. It allows for the creation and destruction of tokens through minting and burning functions. This contract is intended to provide a basic example of token management on the Ethereum blockchain, with public variables to store the token name, abbreviation, and total supply. The contract also includes a mapping to track the balances of different addresses.

## Getting Started

### Installing

1. **Clone the repository:**

    ```
    git clone https://github.com/thesibtainrazza/MyToken.git
    cd MyToken
    ```

2. **Install the necessary dependencies:**

    This contract uses Solidity version 0.8.26. Make sure you have the appropriate version installed.

### Executing program

To deploy and interact with the smart contract, follow these steps:

1. **Compile the contract:**

    Use the Solidity compiler to compile the contract. You can use tools like Remix IDE, Truffle, or Hardhat for this purpose.

2. **Deploy the contract:**

    Deploy the compiled contract to your preferred Ethereum network (local or testnet) using your preferred deployment tool.

3. **Interact with the contract:**

    After deployment, you can interact with the contract using the following functions:

    ```
    // Mint tokens
    function mint(address _address, uint _value) public;

    // Burn tokens
    function burn(address _address, uint _value) public;
    ```

    Example:

    ```
    // Minting 100 tokens to address 0x123...
    MyToken.mint("0x123...", 100);

    // Burning 50 tokens from address 0x123...
    MyToken.burn("0x123...", 50);
    ```

## Help

### Common issues

1. **Balance too low for burning:**
    - Ensure the address has enough tokens to burn.
    - Check the balance of the address using the `balances` mapping.

    ```
    uint balance = MyToken.balances("0x123...");
    ```

2. **Contract not deploying:**
    - Make sure you're using the correct Solidity version (0.8.26).
    - Ensure your deployment tool is configured correctly.

### Helper command

Use the following command to get more information about the contract and its functions:

```
MyToken.help();
```

## Authors

Contributors names and contact info:

- Sibtain Raza
    - GitHub: [@Raza](https://github.com/thesibtainrazza)

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
