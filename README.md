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
- Includes forks from open-source crypto flasher tools:
  - Ethereum-based flashers (adjusted for Tron)
  - BSC token duplicators (for reference)
- Refactored with compliance and logs for internal use

## 📜 Disclaimer
This tool:
- **Does NOT generate real monetary value**
- **Should NOT be used on mainnet to simulate real assets**
- **Is NOT affiliated with Tether (USDT)**

Kryptoken Technology Inc. assumes no liability for any misuse of this codebase.

## 🛡️ Ethical Compliance
This repository and all its components are developed and deployed with the strict purpose of **ethical blockchain testing and research**. Any use outside the intended scope is strictly prohibited.

## 📬 Contact
Kryptoken Technology Inc.  
📍 Makati Executive Tower 3, Pio del Pilar, Makati City, PH  
📧 team@kryptoken.org  
📞 +63 969 104 7538
# FlashUSDT
