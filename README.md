# EchoHarbor

Built for Base

EchoHarbor is a Base-aligned repository intended to act as a compact verification surface for Base network access, wallet onboarding, and read-only RPC operations.

Instead of implementing complex contract logic, the project focuses on confirming that Base tooling, explorers, and chain metadata behave as expected across environments.

## Why EchoHarbor Exists

This repository is designed to:
- Validate Base Mainnet and Base Sepolia connectivity
- Exercise OnchainKit wallet UX flows
- Perform deterministic onchain reads via Viem
- Provide explicit Basescan references for transparency

## Supported Networks

Base Mainnet  
chainId (decimal): 8453  
Explorer: https://basescan.org  
RPC: https://mainnet.base.org  

Base Sepolia  
chainId (decimal): 84532  
Explorer: https://sepolia.basescan.org  
RPC: https://sepolia.base.org  

## Application Logic

Primary file: `app/echoHarbor.ts`

During execution, the application:
- Initializes an OnchainKitProvider bound to the selected Base chain
- Presents wallet connection UX
- Queries Base RPC endpoints for:
  - chainId
  - latest block number
  - native ETH balance for a supplied address
- Surfaces Basescan explorer URLs for manual inspection

## Project Layout

- app/
  - echoHarbor.ts  
    React entry point combining OnchainKit wallet components with Base RPC reads.

Typical repository companions:
- package.json
- tsconfig.json
- index.html / main.tsx
- .env (optional)

## Dependencies

OnchainKit  
Wallet UI components and Base-first primitives  
https://github.com/coinbase/onchainkit  

Viem  
EVM client used for Base JSON-RPC reads  

## Installation & Usage

Requirements:
- Node.js 18+
- Browser environment with wallet support

Install dependencies using your preferred package manager and run the project with a standard React/Vite or Next.js development server.

Optional environment variables:
- VITE_BASE_RPC_URL
- VITE_BASE_SEPOLIA_RPC_URL

## Base Mainnet Deployment

Deployed on Base Mainnet

Network: Base Mainnet  
chainId (decimal): 8453  
Explorer: https://basescan.org  

Deployed contract address:  
your_adress  

Basescan deployment and verification links:
- https://basescan.org/address/your_adress  
- https://basescan.org/address/your_adress#code  

## License

MIT License

## Author

GitHub: https://github.com/drearyhi  
Public contact (email): hisses.dreary02@icloud.com  
Public contact (X): https://x.com/chrisdrylie4  

## Testnet Deployment (Base Sepolia)

As part of pre-production validation, one or more contracts may be deployed to the Base Sepolia test network to confirm correct behavior and tooling compatibility.

Network: Base Sepolia  
chainId (decimal): 84532  
Explorer: https://sepolia.basescan.org  

Contract "structs" address:  
0x2fc184f0bae2e74506c90f3de5f69e18ee0bd0f8  

Deployment and verification:
- https://sepolia.basescan.org/address/0x2fc184f0bae2e74506c90f3de5f69e18ee0bd0f8  
- https://sepolia.basescan.org/0x2fc184f0bae2e74506c90f3de5f69e18ee0bd0f8/0#code  

Contract "Inheritance" address (optional):  
0x67efcff099b4eb091408c01841d0d9239bb312f9  

Deployment and verification:
- https://sepolia.basescan.org/address/0x67efcff099b4eb091408c01841d0d9239bb312f9  
- https://sepolia.basescan.org/0x67efcff099b4eb091408c01841d0d9239bb312f9/0#code  

These testnet deployments provide a controlled environment for validating Base tooling, account abstraction flows, and read-only onchain interactions prior to Base Mainnet usage.
