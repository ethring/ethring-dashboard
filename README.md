Ethring: DeFi Launchpad for Vaults

Ethring is a DeFi launchpad for listing and managing yield strategies (vaults). We simplify launch, monitoring, and scaling of DeFi assets for users and protocols.

⸻

🔹 What Ethring Does
	•	For users: discover, compare, and start DeFi strategies in one click — no bridges, approvals, or complexity.
	•	For protocols: list vaults and LP assets, manage distribution, analytics, and TVL without building your own frontend.

⸻

🎯 Primary Focus — Strategy Listing

Ethring is not just another aggregator. It’s an entry point where strategies get interface, visibility, and users:
	•	Permissionless vault listing (ERC-20, ERC-4626, LP)
	•	Contract verification (with Exponential risk support)
	•	Display in Explorer and Dashboard
	•	Automatic categorization and analytics

Are you a vault curator? We’ve built the infrastructure for you.

⸻

🧩 User Value
	•	One-click execution: launch a strategy without multiple steps (approve → swap → bridge → stake)
	•	Cross-chain access: any asset, any network, no manual switching
	•	Non-custodial: funds remain in underlying protocols
	•	Dashboard: full portfolio view, rewards, and performance
	•	Explorer: research protocols, trends, and metrics

⸻

🛠 Protocol/Curator Value
	•	Ready-to-use frontend for your LP assets
	•	Multi-standard support (ERC-20, ERC-4626, LP models)
	•	Cross-chain distribution (Ethereum, Base, Arbitrum, BNB, Optimism)
	•	Strategy-level analytics and yield tracking
	•	SDK/integration adapter for fast onboarding

⸻

⚙ Platform Components
	•	📊 Dashboard — manage and monitor LP assets
	•	🔍 Explorer — strategy research, APR, TVL
	•	🌉 Router — cross-chain and cross-protocol routing
	•	⚖️ Risk Ratings — powered by Exponential
	•	🔧 One-click executor — bundle actions into one transaction

⸻

🧭 Integration Guide (for protocols)
	1.	Submit your vault via listing form
	2.	Confirm contract & metadata
	3.	Get frontend, explorer visibility, and TVL tracking

📚 Docs: https://ethring.gitbook.io
💻 GitHub SDK/API: https://github.com/ethring

⸻

🚀 Getting Started as a User
	•	Visit ethring.io
	•	Connect your wallet
	•	Select a strategy → click “Deposit” → Done.

⸻


## Setup

```bash
# Install all dependencies
npm i
```

```bash
# Local page with hot reload at http://localhost:5173
npm run dev
```

```bash
# Build for production with minification
npm run build
```

```bash
# Debug build production, use this command to analyze bundle
npm run build:debug
```

```bash
# Build for production and view the bundle analyzer report
npm run build --report
```

```bash
# Playwright e2e test report
npm run test:report
```

## Environments

| Environment Variable | Description                                                                                          |
| -------------------- | ---------------------------------------------------------------------------------------------------- |
| `NODE_ENV`           | Environment mode, can be one of the following values: `development`, `production`, `test`;           |
| `LOG_LEVEL`          | The level of logging, can be one of the following values: `error`, `warn`, `info`, `debug`, `trace`  |
| `CORE_API`           | The main API for obtaining configurations for chains and tokens                                      |
| `TX_MANAGER_API`     | The main API for obtaining transactions for the account, and also for getting the transaction status |
| `DATA_PROVIDER_API`  | The main API for obtaining balance for the account                                                   |
| `BRIDGE_DEX_API`     | The main API for obtaining super-swap transactions                                                   |
| `PROXY_API`          | The main API for obtaining the prices of tokens via the proxy                                        |
| `IS_ANALYZE`         | The main flag for analyzing the bundle for production build                                          |
| `PORTAL_FI_API`      | The main API for make POOL operations                                                                |
| `APPS_API`           | The main API for interacting with the application |

### Important `DATA_PROVIDER_API`

To get the balance for the account, please specify `DATA_PROVIDER_API` in your `.env` file;

## Tests

If you want update snapshot, you need run this code in work dir:

```bash
docker run --rm --network host -v $(pwd):/work/ -w /work/ -it mcr.microsoft.com/playwright:v1.40.0-jammy /bin/bash
npm i
npm run test:e2e:updateSnapshot
```
