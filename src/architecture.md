# Architecture

Marselo is built using **Next.js** as a unified frontend and backend solution, integrating the Cartesi Coprocessor for off-chain computation while ensuring verifiability through Ethereum smart contracts. Below is an overview of the system architecture:

```plaintext
+---------------------------+
|                           |
|   Next.js Frontend/API    |
|   (UI + Backend Logic)    |
|                           |
+------------+--------------+
             |
             v
+------------+--------------+
|                           |
|   Cartesi Coprocessor     |
|                           |
+------------+--------------+
             |
             v
+------------+--------------+
|                           |
|   Ethereum Blockchain     |
|                           |
+---------------------------+
```

### Components
#### 1. **Next.js (Frontend & Backend in One)**
- Provides a seamless user interface for interacting with the platform.
- Manages API requests to fetch blockchain data and send computations to the Cartesi Coprocessor.
- Handles authentication, session storage, and real-time updates.
- Implements backend logic for processing user queries and structuring insights.

#### 2. **Cartesi Coprocessor(python)**
- Executes computationally expensive AI and statistical models off-chain.
- Ensures cryptographic verifiability of computations.
- Retrieves and processes on-chain data, then submits computed insights back to Ethereum smart contracts.
- Acts as a scalable and cost-efficient computation layer, reducing gas fees and blockchain congestion.

#### 3. **Ethereum Blockchain**
- Stores key smart contracts that handle data retrieval, verification, and interaction with decentralized applications.
- Maintains immutable records of analyzed data to ensure transparency.
- Facilitates on-chain validation of AI-generated insights through cryptographic proofs.
- Provides integration points for decentralized finance (DeFi) applications, such as swaps and liquidity pools, in future iterations.

### Workflow
1. **User Interaction (Next.js UI & API)**
   - Users access Marselo via a web interface.
   - The frontend makes API calls to request blockchain data or trigger computations.

2. **Data Retrieval (Ethereum & Smart Contracts)**
   - The system queries Ethereum smart contracts for transaction data, liquidity pool metrics, and token behaviors.
   - The raw data is sent to the Cartesi Coprocessor for further analysis.

3. **Off-Chain Processing (Cartesi Coprocessor)**
   - The Coprocessor executes AI models to analyze blockchain trends.
   - Results are formatted and cryptographically secured before being sent back on-chain.

4. **On-Chain Verification & Storage (Ethereum)**
   - The processed insights are published to the blockchain for transparency.
   - Smart contracts validate the results to ensure accuracy and integrity.

5. **Results Display & API Response (Next.js)**
   - The frontend retrieves verified insights and displays them to users.
   - Additional AI-driven recommendations and predictive analytics are presented in the UI.

## Future Enhancements
- **Expanded Data Sources**: Integration with DEX swap data for improved token analytics.
- **Optimized Computation**: Enhancements in AI efficiency using advanced statistical models.
- **Smart Contract Upgrades**: Enabling more complex governance and user interactions.
