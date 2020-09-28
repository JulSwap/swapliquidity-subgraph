# SwapLiquidity Subgraph

[SwapLiquidity](https://swapliquidity.org/) is a decentralized protocol for automated token exchange on BSC mainnet.

This subgraph dynamically tracks any pair created by the SwapLiquidity factory. It tracks of the current state of SwapLiquidity contracts, and contains derived stats for things like historical data and USD prices.

- aggregated data across pairs and tokens,
- data on individual pairs and tokens,
- data on transactions
- data on liquidity providers
- historical data on SwapLiquidity, pairs or tokens, aggregated by day

## Running Locally

Make sure to update package.json settings to point to your own graph account.


## Key Entity Overviews


#### Token

Contains data on a specific token. This token specific data is aggregated across all pairs, and is updated whenever there is a transaction involving that token.

#### Pair

Contains data on a specific pair.

#### Transaction

Every transaction on SwapLiquidity is stored. Each transaction contains an array of mints, burns, and swaps that occured within it.

#### Mint, Burn, Swap

These contain specifc information about a transaction. Things like which pair triggered the transaction, amounts, sender, recipient, and more. Each is linked to a parent Transaction entity.


