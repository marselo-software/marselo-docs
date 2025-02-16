# Models V1

## Overview
Marselo is an AI-powered blockchain analytics platform that leverages the Cartesi Coprocessor to execute off-chain models while maintaining on-chain integrity. The system currently operates in its **MVP (Minimum Viable Product)** stage, using Remix testnet data to retrieve key blockchain metrics.

## Current Functionality
- **Blockchain Data Retrieval**: Marselo fetches relevant on-chain data from Ethereum testnet using Solidity smart contracts.
- **Off-Chain Computation**: Complex calculations and AI models are executed via the Cartesi Coprocessor, ensuring scalable and efficient processing.
- **Insights & Reports**: The system analyzes token trends, liquidity, and market patterns, presenting structured insights to users.

## Future Enhancements
- **Integration with Swaps**: Future iterations will incorporate decentralized exchanges (DEXs) to retrieve real-time token price, volume, and liquidity data.
- **AI-Driven Agents**: Advanced AI models will detect market anomalies, predict trends, and offer actionable insights for traders and investors.
- **On-Chain Verification**: Although AI models run off-chain, the results will be cryptographically verifiable and stored on-chain for transparency.

## Models and Their Functions
### 1. **Blockchain Data Extractor**
- **Purpose**: Retrieves transaction data, smart contract states, and historical prices.
- **Execution**: Uses Solidity smart contracts to query Ethereum blockchain and fetch raw data.
- **How it Works**:
  - The extractor listens to blockchain events and collects transaction logs.
  - It processes smart contract interactions to analyze asset movements and token approvals.
  - Uses indexing techniques to structure raw blockchain data for easier analysis.
- **Insights Provided**:
  - Historical transaction patterns of specific wallets or tokens.
  - Smart contract interaction trends, including DeFi protocol usage.
  - Anomalies in transaction flow that may indicate wash trading or market manipulation.

### 2. **AI-Based Market Analysis**
- **Purpose**: Identifies trends, anomalies, and patterns in token price movements.
- **Execution**: Runs statistical and machine learning models via Cartesi Coprocessor to analyze large-scale on-chain and off-chain data.
- **How it Works**:
  - Time-series models analyze past price movements to forecast future trends.
  - Machine learning algorithms cluster transaction behaviors to detect whale movements and unusual trading activity.
  - Sentiment analysis on on-chain activity evaluates how transactions reflect broader market sentiment.
- **Insights Provided**:
  - Predictive models estimate short-term and long-term token price fluctuations.
  - Identifies correlations between different token movements and trading volumes.
  - Detects potential pump-and-dump schemes or coordinated market activities.

### 3. **Liquidity & Risk Assessment**
- **Purpose**: Evaluates liquidity depth, token availability, and potential risks in decentralized markets.
- **Execution**: Processes data from DEX liquidity pools, swap transactions, and order books.
- **How it Works**:
  - Tracks liquidity pool reserves to measure available liquidity for different token pairs.
  - Calculates slippage impact based on past trade data and liquidity depth.
  - Monitors large liquidity shifts that could indicate risks such as rug pulls or impermanent loss.
- **Insights Provided**:
  - Risk assessment scores for different tokens based on their liquidity stability.
  - Analysis of liquidity provider behaviors and shifts in liquidity pools.
  - Detection of vulnerabilities in smaller market-cap tokens prone to manipulation.

<div class="warning">
    This project is currently in MVP stage, and we are using testnet data from Remix. In the future, we plan to integrate token swaps to gather more data from the network.
</div>
