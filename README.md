# Flash USDT Simulator (TRC-20 - Tron Network)
**⚠ FOR DEVELOPMENT AND TESTING PURPOSES ONLY ⚠**

This project provides a simulated version of **USDT** (Tether) deployed on the **TRON Network** using TRC-20 standards. It includes flash token functionalities to deliver **non-monetary, fake tokens** to user wallets. 

> 🛑 This project is strictly for internal use, testing, UI/UX validation, education, and development. It is NOT intended for real-world financial transactions or any form of fraud.

## 📌 Features
- Simulates **USDT (Tether)** with:
  - ✅ 6 decimal places
  - ✅ Minting and burning functionality
  - ✅ Based on OpenZeppelin's ERC20 implementation
- Tron Network deployment via:
  - [Tron IDE](https://developers.tron.network/docs/tron-ide)
  - TronBox
- Integration with third-party "crypto flasher" tools for simulated token transfers

## 🚀 Use Case Scenarios
- UI/UX Wallet Testing
- Blockchain app transaction simulations
- TRON wallet functionality validation
- Education, training, or demonstration environments

## 🛠️ Requirements
- Node.js (for TronBox)
- TronLink Wallet (for testing on browser)
- TRON Shasta or Nile Testnet
- OpenZeppelin Contracts (adapted for TRON)

## 🔧 Installation & Setup
1. Clone the repository:
   ```bash
   git clone https://github.com/your-org/flash-usdt-tron.git
   cd flash-usdt-tron
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Compile contracts:
   ```bash
   tronbox compile
   ```

4. Deploy to Testnet:
   ```bash
   tronbox migrate --network shasta
   ```

## 📄 Smart Contract Overview
```solidity
contract MockUSDT is TRC20 {
    constructor() TRC20("USDT Sim", "USDT", 6) {}

    function mint(address to, uint256 amount) public onlyOwner {
        _mint(to, amount);
    }

    function burn(address from, uint256 amount) public onlyOwner {
        _burn(from, amount);
    }
}
```

## 📁 Backups and Forked Flashers
- Includes APK and forks from open-source crypto flasher tools
- Supports different blockchain networks (Ethereum, Binance, Tron)
- Refactored with compliance and logs for internal use

  <!-- First row: 1 image centered -->
<p align="center">
  <img src="https://www.kryptoken.org/wp-content/uploads/2025/07/Screenshot-from-2025-07-10-14-52-21.png" alt="Flash Coin Sender" width="600"/>
</p>

<!-- Second row: 2 images side by side -->
<p align="center">
  <img src="https://www.kryptoken.org/wp-content/uploads/2025/07/WhatsApp-Image-2025-07-10-at-14.58.04.jpeg" alt="Flash USDT Sender1" width="300"/>
  <img src="https://www.kryptoken.org/wp-content/uploads/2025/07/WhatsApp-Image-2025-07-10-at-14.58.041.jpeg" alt="Flash USDT Sender2" width="300"/>
</p>

## 📜 Disclaimer
This tool:
- **Does NOT generate real monetary value**
- **Should NOT be used on mainnet to simulate real assets**
- **Is NOT affiliated with Tether (USDT)**

Kryptoken Technology Inc. assumes no liability for any misuse of this codebase.

## 🛡️ Ethical Compliance
This repository and all its components are developed and deployed with the strict purpose of **ethical blockchain testing and research**. Any use outside the intended scope is strictly prohibited.

## 📬 Contact
Kristoffer Narag | Myrel De Castro

🏛️ Kryptoken Technology Inc.  
📍 Makati Executive Tower 3, Pio del Pilar, Makati City, PH  
📧 team@kryptoken.org  
📞 +63 969 104 7538 | +63 995 562 2499

## 👥 Project Partner
PT Giga Internusa Persada 🇮🇩
# FlashUSDT
