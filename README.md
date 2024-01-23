# DegenToken

## Overview

DegenToken is an Ethereum-based smart contract that represents a token with additional functionality for managing and interacting with iPhones. The contract extends the ERC-20 standard, allowing for basic token operations such as minting, burning, and transferring. Additionally, it introduces specific features for handling iPhones, including charging, redemption, and quantity management.

## Smart Contract Components

### ERC-20 Standard

DegenToken complies with the ERC-20 standard, providing the fundamental functionality for a fungible token on the Ethereum blockchain. Users can transfer, mint, and burn tokens following the standard ERC-20 interface.

### iPhone Management

The contract includes features to manage iPhones, represented by the `phone` struct. iPhones have a charge level and a total enumeration value, which is used in various operations.

### Minting and Burning

Owners of the contract can mint new tokens and burn existing ones. The `mint` function allows the contract owner to create new tokens and distribute them to a specified address. The `burn_` function enables token holders to burn their tokens, reducing the total supply.

### Transferring iPhones

Token holders can transfer iPhones to other addresses using the `transfer_` function. This function ensures that the sender has sufficient iPhones before completing the transfer.

### Setting iPhone Charge and Quantities

The owner can set the charge and total enumeration for a specific iPhone model using the `setIphoneChargeAndQuantities` function. This function helps manage the characteristics of each iPhone type within the contract.

### Redeeming iPhones

Token holders can redeem iPhones by burning a corresponding number of tokens. The `redeemIphone` function checks if the sender has enough tokens and if there are sufficient iPhones available for redemption. If the conditions are met, the operation is completed, and the iPhones are transferred to the user.

## Usage

1. **Deploy Contract:**
   Deploy the DegenToken contract on the Ethereum blockchain.

2. **Mint Tokens:**
   The contract owner can mint new tokens using the `mint` function.

3. **Transfer Tokens:**
   Token holders can transfer tokens to other addresses using the standard ERC-20 `transfer` function.

4. **Set iPhone Characteristics:**
   The owner can set the charge and total enumeration for different iPhone models using the `setIphoneChargeAndQuantities` function.

5. **Redeem iPhones:**
   Token holders can redeem iPhones by burning tokens through the `redeemIphone` function.

6. **Burn Tokens:**
   Token holders can burn their tokens using the `burn_` function.

## Error Messages

- INSUFFICIENT FUNDS!!: Indicates that the user does not have enough tokens to perform the requested operation.
- Iphone name cannot be empty: Ensures that the iPhone name provided is not an empty string.
- Charge must be greater than zero: Requires that the charge value for an iPhone is a positive number.
- Total enumeration must be greater than or equal to zero: Validates that the total enumeration for an iPhone is a non-negative number.
- Insufficient iphone total enumeration: Verifies that there are enough iPhones available for the requested operation.

## License

This smart contract is released under the MIT License. See [LICENSE](./LICENSE) for details.

## Author

Krishna 

km1527771@gmail.com
