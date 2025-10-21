
# CoacoTrace – Somnia AI Hackathon Submission

![Project Banner](./assets/banner.png) <!-- Optional: replace with your image -->

## Overview
CoacoTrace is an on-chain autonomous AI-powered agent designed to improve **supply chain traceability for agricultural products**, starting with cocoa. It leverages blockchain and smart contracts to provide **transparent, immutable, and real-time tracking** of products from farm to consumer. Built for the Somnia AI Hackathon, CoacoTrace combines AI intelligence with decentralized infrastructure to create a trustless and automated system for supply chain monitoring.

## Features
- **Real-time product tracking**: Monitor the movement of cocoa and other agricultural products across the supply chain.
- **Immutable blockchain records**: Store product provenance and transactions securely on-chain.
- **AI-powered automation**: Smart agents detect anomalies, generate reports, and optimize supply chain routes.
- **User-friendly dashboard**: Visualize supply chain data for farmers, distributors, and regulators.
- **Seamless wallet integration**: Supports sBTC transactions via Turnkey Embedded Wallet SDK for payments and incentives.

## Smart Contract
CoacoTrace uses **Solidity smart contracts** deployed on the [Stacks blockchain](https://stacks.co/). Key functionalities include:
- Product registration
- Ownership transfer
- Verification of product authenticity
- Event logging for supply chain milestones

```solidity
// Example snippet
function registerProduct(string memory productId, address owner) public {
    require(products[productId].owner == address(0), "Product already registered");
    products[productId] = Product(productId, owner, block.timestamp);
    emit ProductRegistered(productId, owner);
}git clone https://github.com/<your-username>/coacotrace.git
cd coacotrace
npm install
REACT_APP_API_KEY=your_openai_api_key
REACT_APP_WALLET_KEY=your_turnkey_wallet_key
npm start
# Example: using Stacks CLI
stacks-cli contract deploy --contract-path ./contracts/ProductRegistry.clar
