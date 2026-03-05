# 🟠 OPNET DeFi — Bitcoin L1 

> **DeFi protocol built on OPNET smart contract layer for Bitcoin L1.**  
> Mainnet Live: **17 March 2026** 🚀

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Bitcoin Mainnet](https://img.shields.io/badge/Bitcoin-Mainnet-orange?logo=bitcoin)](https://opnet.org)
[![OPNET](https://img.shields.io/badge/Powered%20by-OPNET-orange)](https://opnet.org)
[![Mainnet](https://img.shields.io/badge/Status-Live%20Mainnet-brightgreen)](https://opnet.org)

---

## 🌟 Overview

OPNET DeFi is a fully on-chain decentralized finance application built on the **OPNET protocol** — the first smart contract layer for Bitcoin. This project enables:

- 🔄 **Token Swaps** — Trade BRC-20 tokens and Runes instantly
- 💧 **Liquidity Pools** — Provide liquidity and earn trading fees
- 🌱 **Staking** — Stake OPNET tokens for up to 31.8% APY
- 🏛️ **Lending** — Borrow and lend BTC-native assets
- 🌉 **Bridge** — Cross-chain asset transfers across 12 networks
- 🗳️ **Governance** — Vote on protocol upgrades

---

## 🔗 Live Demo

**→ [https://your-username.github.io/opnet-defi](https://frankxeth/motochain.git)**

---

## 💼 Supported Wallets

| Wallet | Status | Type |
|--------|--------|------|
| **OPNET Wallet** | ✅ Official | Bitcoin Native L1 |
| UniSat | ✅ Supported | Bitcoin Native |
| OKX Wallet | ✅ Supported | Multi-chain |
| Xverse | ✅ Supported | Bitcoin Native |
| Leather | ✅ Supported | Bitcoin Native |

---

## 📁 Project Structure

```
opnet-defi/
├── index.html              # Main DeFi application
├── src/
│   ├── wallet.js           # Wallet connection logic
│   ├── swap.js             # Swap functionality
│   └── contracts.js        # OPNET smart contract ABIs
├── public/
│   ├── og-image.png        # Social preview image
│   └── favicon.ico         # Site favicon
├── docs/
│   ├── ARCHITECTURE.md     # Technical architecture
│   └── CONTRACTS.md        # Smart contract docs
├── .github/
│   └── workflows/
│       └── deploy.yml      # GitHub Pages auto-deploy
├── README.md               # This file
├── LICENSE                 # MIT License
└── CONTRIBUTING.md         # Contribution guide
```

---

## 🚀 Quick Start

### 1. Clone the Repository
```bash
  git clone https://github.com/frankxeth/motochain.git
cd opnet-defi
```

### 2. Open Locally
```bash
# Option A: Direct open
open index.html

# Option B: Local server (recommended)
npx serve .
# atau
python3 -m http.server 3000
```

### 3. Deploy to GitHub Pages
```bash
git add .
git commit -m "feat: initial OPNET DeFi deployment"
git push origin main
```
Then enable GitHub Pages in Settings → Pages → Source: `main` branch

---

## 🛠️ OPNET Wallet Integration

This project integrates the **official OPNET Wallet SDK**:

```javascript
// Connect OPNET Wallet
async function connectOPNETWallet() {
  if (typeof window.opnet !== 'undefined') {
    const accounts = await window.opnet.requestAccounts();
    const address = accounts[0];
    console.log('OPNET Wallet connected:', address);
    return address;
  } else {
    window.open('https://wallet.opnet.org', '_blank');
  }
}

// Get Balance
async function getBalance(address) {
  const balance = await window.opnet.getBalance(address);
  return balance;
}

// Execute Swap via OPNET Contract
async function executeSwap(fromToken, toToken, amount) {
  const tx = await window.opnet.sendTransaction({
    to: SWAP_CONTRACT_ADDRESS,
    data: encodeSwapData(fromToken, toToken, amount),
  });
  return tx;
}
```

---

## 🏆 Event Participation

This project was built for the **OPNET Mainnet Launch Event — March 2026**.

### Submission Checklist
- [x] Smart contract integration via OPNET SDK
- [x] Multi-wallet support (OPNET, UniSat, OKX, Xverse, Leather)
- [x] Deployed on Bitcoin Mainnet
- [x] GitHub repository public
- [x] Demo URL live
- [x] README complete with setup instructions
- [x] MIT License included

### Event Links
- 🌐 OPNET Official: [https://opnet.org](https://opnet.org)
- 📖 Developer Docs: [https://docs.opnet.org](https://docs.opnet.org)
- 💬 Discord: [https://discord.gg/opnet](https://discord.gg/3KQKVcjE)
- 🐦 Twitter: [@opnet_btc](https://twitter.com/opnetbtc)

---

## 🤝 Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

1. Fork the repo
2. Create feature branch: `git checkout -b feat/my-feature`
3. Commit changes: `git commit -m 'feat: add feature'`
4. Push: `git push origin feat/my-feature`
5. Open a Pull Request

---

## 📄 License

MIT License — see [LICENSE](LICENSE) for details.

---

*Built with ❤️ on Bitcoin · OP_NET L1 · Mainnet on 17 March 2026*
