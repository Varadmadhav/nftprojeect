# Simple NFT Marketplace - README

## Vision

The **Simple NFT Marketplace** is a decentralized platform aimed at providing a straightforward and efficient way to list and buy NFTs (Non-Fungible Tokens) using the Aptos blockchain. It is designed to offer ease of use for creators and collectors while ensuring secure transactions using the Aptos Coin (APT). Our goal is to foster a user-friendly environment where anyone can participate in the growing NFT space with minimal technical barriers. 

## Features

### 1. **NFT Listing**
   - Creators can list their NFTs for sale by providing the name of the NFT and setting a price.
   - The `list_nft` function allows the seller to move the NFT into their account and mark it as available for purchase.

### 2. **Buying NFTs**
   - Collectors (buyers) can purchase listed NFTs using Aptos Coin (APT).
   - The `buy_nft` function ensures that the buyer pays the correct price and updates the ownership status of the NFT.
   - Once purchased, the NFT is no longer listed for sale.

### 3. **Secure Payment System**
   - All payments are securely transferred using Aptos Coin (APT) and Aptos’ built-in coin module.
   - The platform ensures that the seller receives the full amount for the NFT before finalizing the sale.

### 4. **Error Handling**
   - **ENFT_ALREADY_LISTED**: Prevents NFTs from being listed multiple times.
   - **ENFT_NOT_LISTED**: Ensures that buyers can only purchase NFTs that are available for sale.
   - **EINSUFFICIENT_FUNDS**: Protects the transaction process by preventing underfunded purchases.

## Smart Contract Overview

### Modules Used:
- **`std::signer`**: Handles ownership and signing functionalities.
- **`aptos_framework::coin`**: Manages the Aptos Coin token and its transfer between accounts.
- **`aptos_framework::aptos_coin::AptosCoin`**: Specifies the use of Aptos' native coin as the currency for buying NFTs.
- **`std::string::String`**: Manages the NFT name and other string data.

### Core Structures:
- **`ListedNFT`**: This struct holds the details of the NFT (creator's address, price, name, and listing status).
- **`MarketplaceData`**: Tracks overall marketplace information, such as the number of listings.

## Future Scope

While the **Simple NFT Marketplace** provides a basic foundation for listing and buying NFTs, there are several areas for expansion and improvement:

1. **Royalty Support**: Enable creators to receive a percentage of the sale whenever an NFT is resold.
2. **NFT Metadata Storage**: Integrate a method to link NFTs to metadata such as images, descriptions, or external files using decentralized storage solutions.
3. **Auction Functionality**: Implement auction-based sales to allow buyers to bid on NFTs.
4. **Cross-Chain Integration**: Expand support for cross-chain transactions, enabling the use of other cryptocurrencies or the listing of NFTs from other blockchains.
5. **Enhanced Security Features**: Introduce multisig wallets and smart contract audits to increase security for high-value transactions.
6. **Search and Filter Options**: Provide users with the ability to search and filter NFTs based on various attributes (e.g., price, creator, or rarity).
7. **Fractional Ownership**: Allow multiple buyers to co-own high-value NFTs by purchasing fractions of an NFT.

## Conclusion

The **Simple NFT Marketplace** offers an easy-to-use framework for listing and purchasing NFTs on the Aptos blockchain. While simple, this project sets the stage for future enhancements and growth, as we aim to evolve the platform into a fully-featured NFT marketplace with auctioning, royalties, and cross-chain support.

