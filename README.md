# dropdead.me: Deadman Switch on Chain

This project outlines the development of a decentralized "Deadman Switch" application, branded as **dropdead.me**. The application allows users to upload encrypted information to the blockchain and define triggers that will release the information if a condition is unmet (e.g., failing to interact with the contract at predefined intervals). While the initial implementation leverages the NEAR Protocol, the app's scope extends beyond a single smart contract, encompassing a full-featured decentralized application.

## Feature Overview

### Upload and Encrypt Information
- Users can securely upload sensitive information directly through the frontend application.
- Information is encrypted client-side before being stored on the blockchain, ensuring privacy and security.
- Supports any type of user-provided data (e.g., text, keys, messages, or small files).

### Define Triggers
- Triggers allow users to define conditions for releasing their information.
- Initial implementation supports time-based triggers where users must interact with the contract at specific intervals.
- Future iterations could include more sophisticated triggers such as:
  - Email reminders.
  - Activity on linked accounts.
  - Multi-signature approval mechanisms.

### Release Mechanism
- If the user-defined trigger condition is unmet (e.g., no interaction within the time frame), the contract will release the encrypted information.
- Released data is logged in the blockchain or made accessible via predefined mechanisms.
- Users retain the ability to cancel or update their triggers before they are met.

### Monetization Model
- Users pay a small NEAR fee to upload information and set triggers.
- A percentage of the NEAR deposit is retained as a service fee by the platform.
- Remaining balance is used to cover transaction costs and other operational expenses.

### Frontend Application
- User-friendly interface for:
  - Logging in with a NEAR wallet.
  - Uploading encrypted information.
  - Defining and managing triggers.
  - Monitoring the status of their data and triggers.
- Provides client-side encryption and decryption functionality using standard cryptographic libraries (e.g., `crypto-js` or Web Crypto API).

---

## Technology Stack Overview

### Blockchain and Smart Contract
- **Blockchain Platform:** NEAR Protocol
  - Chosen for its low fees, high scalability, and developer-friendly environment.
- **Smart Contract Language:** Rust
  - High-performance and secure programming language suitable for writing robust smart contracts.
- **Smart Contract Framework:** NEAR SDK
  - Provides tools and abstractions for developing, testing, and deploying contracts on NEAR.
- **Data Storage:** On-chain storage for encrypted information using NEAR's key-value storage.
  - Encrypted data is stored directly in the contract's persistent storage.

### Frontend Application
- **Frontend Framework:** React.js
  - Lightweight and widely adopted for building interactive user interfaces.
- **Wallet Integration:** NEAR Wallet
  - Enables users to authenticate and interact with the blockchain seamlessly.
- **Encryption Library:** `crypto-js` or Web Crypto API
  - Handles client-side encryption and decryption of sensitive information before interacting with the blockchain.

### Monetization and Payment Handling
- **Native Token:** NEAR
  - Users pay NEAR tokens to interact with the application.
- **Fee Mechanism:** Implemented within the smart contract to deduct a small percentage of user deposits as platform revenue.

### Testing and Deployment
- **Testnet:** NEAR Testnet for initial development and testing.
- **Mainnet:** NEAR Mainnet for production deployment.
- **Hosting:** Frontend hosted on platforms like Vercel, Netlify, or GitHub Pages for high availability and low maintenance.

### Future Extensions
- **Off-Chain Storage:** Integrate IPFS or similar decentralized storage solutions for handling larger files while storing references on-chain.
- **Trigger Notifications:** Add notification mechanisms like email or SMS to remind users before trigger deadlines.
- **Advanced Triggers:** Incorporate multi-user and conditional logic triggers to expand functionality.

---

This detailed overview provides a comprehensive understanding of the planned features and technology stack for **dropdead.me**, the Deadman Switch on Chain.
