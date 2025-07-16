# Neon Dev Bootcamp – Week 1

## MemeLaunchpad and Raydium Swap: Customized Version

This project demonstrates the deployment and testing of the MemeLaunchpad contract on Neon EVM, including token sales and Raydium pool interactions on Solana. As part of Neon Bootcamp Week 1, we explored the full flow from deploying contracts to performing token swaps and collecting fees.

---

## What We Did

1. Set up the development environment with Hardhat, Solana SDK, and Raydium SDK.
2. Deployed the **BondingCurve** and **MemeLaunchpad** contracts to Neon Devnet.
3. Ran a series of tests covering:

   * Creating a token sale
   * Buying tokens below and above the funding goal
   * Swapping tokens in a Raydium CPMM pool
   * Collecting token sale and liquidity pool fees
4. Modified specific parameters in the tests to fit our customized version:

   * Changed the **token purchase amounts**:

     * `buy()` below funding goal: `0.1 SOL` (from `0.01 SOL`)
     * `buy()` above funding goal: `1.5 SOL` (from `0.15 SOL`)
   * Updated the **fee percentage** for MemeLaunchpad from `1%` to `5%`.

---

## How We Ran It

1. Funded wallets on Neon Devnet with NEON and Solana Devnet with SOL.
2. Configured `ANCHOR_WALLET` and `config.js` with our wallet details.
3. Deployed contracts and executed tests using Hardhat:

```bash
npx hardhat test
```

4. Observed the creation of a Raydium pool, WSOL and token transfers, and fee collection flows in the console output.

---

## Outcome

We successfully executed all steps and confirmed the interaction between Neon EVM and Solana via composability. This included deploying contracts, managing token sales, performing swaps on Raydium, and collecting fees.

Most importantly, we gained a clear understanding of how Neon abstracts Solana operations for Solidity developers and how to customize contract parameters for our own use case.

