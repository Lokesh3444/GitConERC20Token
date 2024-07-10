# GitConERC20Token

### Overview

This document describes the functionalities and features of a custom ERC20 token smart contract. The contract is built using OpenZeppelin's ERC20 contract and includes additional functionalities for minting, transferring, and burning tokens.

### Features

1. **Minting Tokens**
   - **Function:** `mint`
   - **Description:** Allows the contract owner to mint new tokens and assign them to a specified address.
   - **Access Control:** Only the contract owner can call this function.

2. **Transferring Tokens**
   - **Function:** `transferTokens`
   - **Description:** Allows any user to transfer tokens from their own balance to another address.
   - **Access Control:** Any user can call this function.

3. **Burning Tokens**
   - **Function:** `burnTokens`
   - **Description:** Allows any user to burn tokens from their own balance, reducing the total supply.
   - **Access Control:** Any user can call this function.

### Contract Details

- **Owner:** The address that deploys the contract is set as the owner. The owner has exclusive rights to mint new tokens.
- **Token Name and Symbol:** The contract constructor accepts parameters for the token's name and symbol, which are set during deployment.
- **Access Control:** 
  - The `onlyOwner` modifier is used to restrict access to the minting function, ensuring only the owner can mint new tokens.

### Functions

#### mint
- **Description:** Mints new tokens and assigns them to a specified address.
- **Parameters:**
  - `_to` (address): The address to receive the newly minted tokens.
  - `_amount` (uint256): The amount of tokens to mint.
- **Access Control:** Only the owner can call this function.

#### transferTokens
- **Description:** Transfers tokens from the caller's address to a specified address.
- **Parameters:**
  - `_to` (address): The recipient's address.
  - `_amount` (uint256): The amount of tokens to transfer.
- **Access Control:** Any user can call this function.

#### burnTokens
- **Description:** Burns a specified amount of tokens from the caller's address.
- **Parameters:**
  - `_amount` (uint256): The amount of tokens to burn.
- **Access Control:** Any user can call this function.

### Usage

1. **Deploying the Contract:**
   - Deploy the contract using a Solidity-compatible environment, providing the desired token name and symbol as constructor arguments.

2. **Minting Tokens:**
   - Only the owner can mint tokens by calling the `mint` function with the recipient's address and the amount of tokens to mint.

3. **Transferring Tokens:**
   - Any user can transfer their tokens to another address by calling the `transferTokens` function with the recipient's address and the amount of tokens to transfer.

4. **Burning Tokens:**
   - Any user can burn their tokens by calling the `burnTokens` function with the amount of tokens to burn.

### Conclusion

This custom ERC20 token smart contract provides basic functionalities for minting, transferring, and burning tokens, with appropriate access control to ensure only the owner can mint new tokens. The contract is built using OpenZeppelin's ERC20 contract, ensuring compatibility and security.
