# NEAR-Ethereum Stablecoin Swap Proof-of-Concept
### Theme: Infrastructure
### Prize: $1,000

## Objective 
Design a proof-of-concept demonstrating the core mechanisms for initiating a stablecoin swap (e.g., USDC) between the NEAR and Ethereum blockchains. In particular, focus on the communication layer and a frontend interface for initiating a swap request.

### Key Targets for the Hackathon
1. **Communication Protocol Sketch:**  
   Outline a secure messaging system or framework to facilitate cross-chain swap requests.

2. **Basic Frontend:**  
   Build a simple interface to trigger a swap request, showcasing the user flow.

3. **Conceptual Architecture:**  
   Diagram how the communication protocol would integrate with existing or potential liquidity providers to complete the swap.

### Data Samples & Sources:
- **On-chain (NEAR):**  
  Explore block explorers like [NEARBlocks](https://nearblocks.io/) to understand available data (transactions, token transfers, smart contract state).

- **Ethereum Data:**  
  Consider APIs from data providers like Etherscan ([Etherscan](https://etherscan.io/)) or node providers like Infura for relevant Ethereum state.

- **Simulated Swap Data:**  
  Generate sample swap requests including token types, amounts, and user wallet addresses (both NEAR and Ethereum).

### Tech Stack Recommendations
- **Smart Contracts:**  
  Rust (NEAR's primary language) or AssemblyScript.

- **Frontend:**  
  JavaScript/TypeScript with frameworks like React or Vue.

- **Cross-Chain Communication:**  
  Investigate libraries or protocols specializing in NEAR-Ethereum bridging (e.g., Aurora, Rainbow Bridge)
