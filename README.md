# Ethring: DeFi Launchpad for Vaults

**Ethring** is a DeFi launchpad for listing and managing yield strategies (vaults). We simplify launch, monitoring, and scaling of DeFi assets for users and protocols.

---

## 🔹 What Ethring Does

* **For users**: Discover, compare, and launch DeFi strategies in one click — no bridges, approvals, or complexity.
* **For protocols**: List vaults and LP assets, manage distribution, analytics, and TVL without building your own frontend.

---

## 🎯 Primary Focus — Strategy Listing

Ethring is not just another aggregator. It’s an entry point where strategies gain interface, visibility, and user traction:

* ✅ Permissionless vault listing (ERC-20, ERC-4626, LP tokens)
* ✅ Smart contract verification (w/ Exponential risk data)
* ✅ Automatic categorization and analytics
* ✅ Display in Explorer and Dashboard

Are you a vault curator? We’ve built the infrastructure for you.

📩 **Submit your vault here**: [https://ethring.fibery.io/@public/forms/aVgQHFkr](https://ethring.fibery.io/@public/forms/aVgQHFkr)

---

## 🧩 What Users Get

* ⚡ **One-click execution**: Combine all actions (swap → bridge → stake) into a single transaction
* 🌐 **Cross-chain access**: Use any asset across chains, no manual switching
* 🔒 **Non-custodial**: Funds stay in original protocols
* 📊 **Dashboard**: Track positions, rewards, and APY in one place
* 🔍 **Explorer**: Discover strategies and compare performance

---

## 🛠 What Protocols/Curators Get (soon)

* 🧱 **Ready-to-use frontend** for vaults and LP strategies
* 🔄 **Support for ERC-20, ERC-4626, LP standards**
* 🌉 **Cross-chain distribution**: Ethereum, Base, Arbitrum, BNB, Optimism
* 📈 **Analytics and TVL tracking** per strategy
* 🔌 **SDK & integration adapters** for fast onboarding

---

## ⚙ Platform Components

| Component      | Function                                                  |
| -------------- | --------------------------------------------------------- |
| **Dashboard**  | Real-time overview of vaults, positions, rewards          |
| **Explorer**   | Strategy discovery and protocol research                  |
| **Router**     | Multi-step cross-chain transactions (bridge, swap, stake) |
| **Risk Layer** | Strategy-level safety signals powered by Exponential      |
| **Executor**   | Bundles all actions into a single smart transaction       |

---

## 🧭 Integration Flow (For Protocols)

1. Submit vault via [this form](https://ethring.fibery.io/@public/forms/aVgQHFkr)
2. Verify contract metadata and logo
3. Your strategy appears in Explorer, Dashboard, and Routing system

📚 Docs: [https://ethring.gitbook.io](https://ethring.gitbook.io)
💻 GitHub SDK/API: [https://github.com/ethring](https://github.com/ethring)

---

## 🚀 Getting Started (For Users)

1. Go to [ethring.io](https://ethring.io)
2. Connect your wallet
3. Pick a strategy → Click `Deposit` → You’re in

---


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
