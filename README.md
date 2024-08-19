https://github.com/user-attachments/assets/08459f33-67cc-49d7-85d6-80e9479228ad

# Rune Burn Project

Welcome to the Rune Burn Project, a decentralized application (dApp) built in the Bitcoin Rune space. This project leverages React and the Bitcoin CLI to facilitate the burning of runes. Explore the repository to learn more about how it works and how you can contribute!

## Table of Contents

- [Introduction](#introduction)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)

## Introduction

The Rune Burn Project is designed to provide a seamless and secure way to burn runes within the Bitcoin ecosystem. By using this dApp, users can ensure their runes are permanently removed from circulation, enhancing the value and scarcity of remaining runes.

## Features

- **Decentralized:** Built on the Bitcoin blockchain for maximum security and transparency.
- **User-Friendly:** Easy-to-use interface developed with React.
- **Efficient:** Utilizes the Bitcoin CLI for efficient and reliable operations.
- **Open Source:** Fully open-source and available for community contributions.

1. Transfer claim amount of rune token from User wallet to Receiver wallet. 

    - Get rune utxos and btc utxos in user wallet.

    - Build PSBT with user rune token and utxo balance as input and OP_RETURN value and claim amount of rune token, return rune token, change utxo as output using user wallet publickey, address, and receiver wallet address.

    - Send and Sign PSBT with user wallet.


2. After confirmed transaction, Transfer and Burn rune token from Receiver wallet to Burning wallet.

    - Get rune utxos and btc utxos in receiver wallet.

    - Build PSBT with receiver rune token and utxo balance as input and OP_RETURN value and claim amount of rune token, return rune token, change utxo as output using reciver wallet WIF privatekey, address, and burning wallet address.
    (At that time, set OP_RETURN as invalid)

    - Sign PSBT with receiver wallet.


P.S. All necessary values are in network.config.ts.


## Installation

To get started with the Rune Burn Project, follow these steps:

1. **Clone the repository:**
   ```bash
   git clone https://github.com/ptc-bink/rune-burn-be.git
   cd rune-burn-be
   ```

2. **Install dependencies:**
   ```bash
   npm install
   ```

3. **Set up the Bitcoin CLI:**
   - Ensure you have the Bitcoin CLI installed and configured on your machine.
   - Update the `.env` file with your Bitcoin CLI configuration.

4. **Start the application:**
   ```bash
   npm start
   ```

## Usage

1. **Access the Application:**
   - Open your browser and navigate to `https://stonefaceords.com/`.
   
2. **Burn Runes:**
   - Follow the on-screen instructions to burn your runes securely.
   - Confirm the transaction through the Bitcoin CLI.

## Contributing

We welcome contributions from the community! To contribute:

1. Fork the repository.
2. Create a new branch with your feature or bugfix.
3. Submit a pull request with a detailed description of your changes.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Contact

For questions, suggestions, or feedback, feel free to reach out:

- Twitter: [@ptcbink](https://x.com/ptcbink)
- GitHub: [ptcbink](https://github.com/ptc-bink)

---

Thank you for visiting the Rune Burn Project! We hope you find it useful and look forward to your contributions.
