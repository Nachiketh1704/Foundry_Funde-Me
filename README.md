# Foundry Fund Me

Foundry Fund Me is a decentralized crowdfunding platform built with Solidity and the Foundry framework. It enables users to create and manage fundraising campaigns on the Ethereum blockchain, ensuring transparency and security through smart contracts.

## Features

- **Create Campaigns**: Users can initiate fundraising campaigns with a specified goal and deadline.
- **Contribute Funds**: Supporters can contribute ETH to active campaigns.
- **Withdraw Funds**: Campaign creators can withdraw funds once the goal is met.
- **Refunds**: If a campaign does not meet its goal by the deadline, contributors can withdraw their funds.

## Prerequisites

Before setting up the project, ensure you have the following installed:

- **Git**: Version control system.
- **Foundry**: Ethereum development toolkit.

## Installation

1. **Clone the Repository**:

   ```bash
   git clone https://github.com/Nachiketh1704/Foundry_Funde-Me.git
   cd Foundry_Funde-Me
   ```

2. **Install Dependencies**:

   ```bash
   forge install
   ```

3. **Build the Project**:

   ```bash
   forge build
   ```

   Alternatively, you can use the MakeFile commands for convenience:

   ```bash
   make install  # Installs dependencies
   make build    # Builds the project
   ```

## Usage

### Running Tests

Execute the following command to run the test suite:

```bash
forge test
```

Alternatively, use the MakeFile:

```bash
make test
```

### Deployment

To deploy the smart contracts:

1. **Start a Local Ethereum Node**:

   ```bash
   anvil
   ```

2. **Deploy Contracts**:

   ```bash
   forge script script/DeployFundMe.s.sol --rpc-url http://localhost:8545 --private-key <your_private_key>
   ```

   Or use the MakeFile for simplified deployment:

   ```bash
   make deploy RPC_URL=http://localhost:8545 PRIVATE_KEY=<your_private_key>
   ```

Replace `<your_private_key>` with your Ethereum account's private key.

## MakeFile Commands

The following commands are defined in the `MakeFile` to streamline common tasks:

- `make install`: Installs project dependencies.
- `make build`: Builds the project.
- `make test`: Runs the test suite.
- `make deploy RPC_URL=<url> PRIVATE_KEY=<key>`: Deploys the project to a specified RPC endpoint.

## Contributing

Contributions are welcome! Please fork the repository and create a pull request with your changes.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Acknowledgments

- Inspired by the [Cyfrin Foundry Fund Me project](https://github.com/Cyfrin/foundry-fund-me-cu).
- Utilizes Chainlink Price Feeds for ETH to USD conversions.

---