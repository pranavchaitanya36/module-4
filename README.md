# CricketToken 

## Overview

CricketToken is a simple ERC-20 token smart contract implemented in Solidity. The contract provides functionality for minting, burning, and transferring tokens. Additionally, it introduces a unique feature allowing users to redeem tokens for specific cricket-related materials.

## Features

### ERC-20 Standard
The CricketToken contract follows the ERC-20 standard, providing basic functionalities such as transferring tokens, checking balances, and approving spending.

### Minting and Burning
The contract owner can mint new tokens and burn existing ones. Minting is the process of creating new tokens and assigning them to a specified address, while burning involves destroying a certain amount of tokens.

### Material Redemption
CricketToken introduces the ability to redeem tokens for cricket-related materials. Each material has an associated cost, and users can exchange their tokens for these materials. The supported materials include:
- Cricket Bat
- Cricket Ball
- Cricket Gloves
- Cricket Helmet

### Ownership
The contract utilizes the Ownable library, ensuring that certain functions, such as minting, can only be executed by the contract owner.

## Getting Started

1. **Deployment**
   - Deploy the contract to the Ethereum blockchain, specifying the initial owner's address.
   
2. **Minting Tokens**
   - The contract owner can mint new tokens using the `mint` function, providing the recipient's address and the number of tokens to be minted.

3. **Burning Tokens**
   - Users can burn their own tokens using the `burn` function, destroying a specified amount of tokens.

4. **Material Redemption**
   - Users can redeem tokens for cricket materials by calling the `redeemMaterial` function and specifying the desired material. The supported materials and their costs are predefined.

5. **Token Transfer**
   - Users can transfer tokens to another address using the `transferTokens` function, providing the recipient's address and the amount of tokens to be transferred.

## Example Usage

```solidity
// Deploy the contract
CricketToken cricketToken = new CricketToken(msg.sender);

// Mint tokens to a specific address
cricketToken.mint(addressToMint, 100);

// Burn tokens
cricketToken.burn(50);

// Redeem cricket material
cricketToken.redeemMaterial("CRICKET_BAT");

// Transfer tokens to another address
cricketToken.transferTokens(addressToTransfer, 30);
```

## Events

The contract emits the following event:
- `MaterialRedeemed`: Triggered when a user redeems tokens for a cricket material. It includes the account address, the redeemed material, and the associated cost.

