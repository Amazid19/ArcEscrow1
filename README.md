# ArcEscrow1
demo 2
# ArcEscrow System - Demo 2

This is a secure Escrow Smart Contract system implemented with a frontend UI using `ethers.js`. It allows a designated buyer to deposit USDC into the escrow, which can then be released to the seller or refunded back to the buyer.

## 📌 Deployment Details

- **Escrow Contract Address:** `0x675737C2e0F5bFA2feE955e6e1F32b12b4402b52`
- **USDC Token Address:** `0x3600000000000000000000000000000000000000`

## 👥 Setup Participants

- **Buyer Wallet:** `0xeF2b94566BE5F10276042F7BaBB54985EE119C95`
- **Seller Wallet:** `0x0814D1586F528db4023A6860cf9BE6EDDDE765d1`

## 🚀 How it Works (Deposit Process)

1. **Wallet Connection:** The system automatically prompts the user to connect their MetaMask wallet.
2. **Buyer Verification:** The contract strictly restricts the deposit function to the designated **Buyer (`0xeF2b...`)**. If any other wallet is connected, the UI will block the transaction.
3. **USDC Allowance (Approve):** Since this is an ERC20 token transaction, the frontend automatically checks the current allowance. If it's insufficient, it will first trigger a MetaMask pop-up to **Approve** the escrow contract to spend the required USDC.
4. **Escrow Deposit:** After successful approval, the main **Deposit** transaction is initiated, moving the USDC securely from the buyer's wallet into the contract.

## 🛠️ Tech Stack

- **Smart Contract:** Solidity (^0.8.20), OpenZeppelin (SafeERC20, IERC20)
- **Frontend:** HTML5, CSS3, JavaScript (Ethers.js v5)
