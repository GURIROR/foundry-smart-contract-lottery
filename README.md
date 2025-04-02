# 🎰 Foundry Smart Contract Lottery

A decentralized lottery system built with Solidity and Foundry. Integrates Chainlink VRF for provable randomness and Chainlink Automation for automated execution. Built as part of the Cyfrin Updraft security and development course.

## Features

- Chainlink VRF v2 for randomness  
- Chainlink Automation to automate winner selection  
- Configurable for multiple networks (local, testnet, mainnet)  
- Foundry-based testing framework  
- Secure and optimized smart contract design  

## Getting Started

### Prerequisites

- Foundry (https://book.getfoundry.sh/getting-started/installation)  
- Git  
- RPC provider like Infura or Alchemy  
- A funded wallet and private key  

### Clone & Install

git clone https://github.com/GURIROR/foundry-smart-contract-lottery.git  
cd foundry-smart-contract-lottery  
forge install

### Environment Setup

Create a `.env` file in your root folder with the following content:

SEPOLIA_RPC_URL=https://sepolia.infura.io/v3/YOUR_PROJECT_ID  
PRIVATE_KEY=your_private_key  
ETHERSCAN_API_KEY=your_etherscan_api_key  
CHAINLINK_SUBSCRIPTION_ID=your_subscription_id

Never share your real `.env` file. Use `.env.example` to show the structure.

### Compile Contracts

forge build

### Run Tests

forge test -vv

### Deploy (example: Sepolia)

forge script script/DeployRaffle.s.sol:DeployRaffle --rpc-url $SEPOLIA_RPC_URL --broadcast --verify -vvvv

## Project Structure

script/           - Deployment scripts  
src/              - Solidity smart contracts  
test/             - Unit and staging tests  
foundry.toml      - Foundry configuration  
.env.example      - Environment variable structure  

## Learning Goals

- Understand Chainlink VRF and Automation integration  
- Write full test coverage in Solidity  
- Structure upgradable, secure, audit-friendly contracts  
- Practice Foundry CLI workflows and deployment  

## License

MIT © 2025 

## Acknowledgements

- Cyfrin Updraft Course  
- Foundry by Paradigm  
- Chainlink Documentation

