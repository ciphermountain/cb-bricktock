# Description

Create an NPM module that connects to a Metamask wallet, searches for a specified ERC-1155 token type in the wallet, and provides functions to return that token's metadata. The goal of this module is to provide a permissions mechanism using NFTs for selling specific currencies on the exchange.

Subject | Detail
------ | -------
Bounty | 250,000 CMTN
Subjects | JavaScript, Web3
Languages | TS, JS
Tools | npm, rollup, jest

# Acceptance Criteria

- When the NPM module is installed in a project and included, the module provides the function `canSellCurrency` with an input of a string currency symbol and a boolean return
- When the NPM module is installed in a project and included, the module provides the function `registerOauth` with an input of a string currency symbol and an output of the NFT type and address
- When the function `canSellCurrency` is called with no input, an error is returned indicating an input is required
- When the function `canSellCurrency` is called with a valid input and no Metamask connected, an error is return indicating a wallet is required
- When the function `canSellCurrency` is called with a valid input and a Metamask wallet connected and no ERC-1155 token type for the specified currency symbol, the function outputs a false response
- When the function `canSellCurrency` is called with a valid input, a Metamask wallet connected, and an ERC-1155 token of the appropriate type for the currency provided, the function outputs a true response
- When the function `registerOauth` is called with no input, an error is returned indicating an input is required
- When the function `registerOauth` is called with a valid input and no Metamask connected, an error is returned indicating a wallet is required
- When the function `registerOauth` is called with a valid input and a Metamask wallet connected and no ERC-1155 token type for the specified currency symbol, an error is returned indicating inadequate permissions
- When the function `registerOauth` is called with a valid input, a Metamask wallet connected, and an ERC-1155 token of the appropriate type for the currency provided, the function returns the NFT type and address

## Documentation

- [ERC-1155](https://eips.ethereum.org/EIPS/eip-1155)
- [Metamask Docs](https://docs.metamask.io/guide/)
