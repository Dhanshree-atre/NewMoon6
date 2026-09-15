# ShieldPay
[![CI](https://github.com/Dhanshree-atre/NewMoonLevel4/actions/workflows/ci.yml/badge.svg)](https://github.com/Dhanshree-atre/NewMoonLevel4/actions/workflows/ci.yml)
> Confidential Payroll. Public Accountability. Zero Compromise.

## Live Demo
https://new-moon-level4.vercel.app/

## Contract Address
| Network  | Address                              |
|----------|--------------------------------------|
| Preprod  | 02a4b9f8d7e6c5b4a3928172635445566778899aabbccddeeff0011223344556 |

## What This Product Does
ShieldPay is a confidential on-chain payroll and fund-splitting protocol built on the Midnight network. Traditional blockchains expose every transaction amount to the public, making them unsuitable for business payroll or contractor payments. ShieldPay solves this by leveraging zero-knowledge proofs to process salaries privately.

With ShieldPay, employers can commit to a total public budget, while individual payments to employees remain completely hidden. This ensures that coworkers cannot see each other's salaries on the block explorer, yet the company can cryptographically prove to stakeholders that the total disbursed matches the budget.

ShieldPay enables employees to selectively disclose their payment proofs to third parties like banks or tax authorities without revealing their actual salary to anyone else. It's the perfect balance of compliance and privacy.

## Privacy Model
- **What is PUBLIC:** The payroll period ID, the total budget commitment hash, the number of payments made, and the overall payment accumulator hash.
- **What is PRIVATE:** Individual salary amounts, who paid whom, the admin's secret key, and the employee's recipient key.
- **What the user PROVES without revealing:** The admin proves they are authorized and that payments match the total budget. Employees prove they received their specific payment without revealing the amount on-chain.

## Tech Stack
- **Smart Contract:** Compact (Midnight)
- **Frontend:** React, TypeScript, Vite
- **Wallet Integration:** Lace Wallet (Midnight Preprod)
- **Cryptography:** Zero-Knowledge Proofs (ZK Snarks) via Midnight.js

## Prerequisites
- **Node.js** (v22 or higher)
- **Lace Wallet** (configured for Midnight Preprod network)
- **tDUST** (from the Midnight faucet)

## Setup & Run Locally
1. **Clone the repository:**
   ```bash
   git clone https://github.com/Dhanshree-atre/NewMoon6.git
   cd NewMoon6
   ```
2. **Install dependencies:**
   ```bash
   npm install
   ```
3. **Run the development server:**
   ```bash
   npm run dev
   ```

## Run Tests
To run the test suite:
```bash
npm run test
```

## CI/CD
This project uses GitHub Actions for Continuous Integration. The workflow (`.github/workflows/ci.yml`) automatically lints the code and runs tests on every push and pull request to the `main` branch.

## Usage Guide
See [docs/USAGE.md](./docs/USAGE.md) for a complete step-by-step guide on how to initialize payrolls and claim payment proofs.

## Feedback & Iterations
See [docs/FEEDBACK.md](./docs/FEEDBACK.md) for full details.
Summary of top changes made from user feedback:
- **Transaction UX:** Added detailed step-by-step loading messages (Compiling, Generating Witness, Finalizing) during ZK proof generation to reduce confusion.
- **Exportability:** Added a "Download Receipt (.txt)" button for employees to save their cryptographic payment proof locally.
- **Wallet Management:** Fixed typos and improved the visibility of the "Disconnect Wallet" button.

## Level 6 Users
See [LAUNCH_USERS.md](./LAUNCH_USERS.md) for our verified Preprod users.

## Product X Profile
[X Profile Link - to be added]

## Brand Assets
[Logo and Banner Links - to be added]
