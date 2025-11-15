# DimensionlessDevelopments CrossBorderPaymentProcessor

A secure, programmable payment processor built on the Arc blockchain, designed for cross-border stablecoin transactions with advanced MEV protection and dynamic routing capabilities.

## Overview

CrossBorderPaymentProcessor by DimensionlessDevelopments is a smart contract implementation that enables secure, automated cross-border payments using USDC and EURC stablecoins. The contract features advanced MEV protection, dynamic routing optimization, and automated currency conversion capabilities.

## Features

* **Multi-Currency Support**: Handles USDC and EURC with extensible currency support
* **MEV Protection**: Implements dynamic timing and trusted relayer mechanisms
* **Dynamic Routing**: Optimizes transaction paths based on amount and conditions
* **Automated Currency Conversion**: Seamless conversion between supported currencies
* **Conditional Settlement**: Ensures guaranteed delivery or refund
* **Event Emissions**: Comprehensive transaction tracking and monitoring

## Installation

```bash
# Install dependencies
npm install @openzeppelin/contracts @circle-fin/bridge-kit

# Compile the contract
npx hardhat compile
```

## Usage

### Deploying the Contract

```bash
# Deploy to Arc testnet
npx hardhat run scripts/deploy.js --network arctestnet
```

### Initiating a Payment

```solidity
function initiateProtectedPayment(
    address recipient,
    uint256 amount,
    string memory currency,
    uint256 customMinExecutionTime
) external nonReentrant {
    // Payment logic
}
```

### Checking Transaction Status

```solidity
function getTransactionStatus(bytes32 paymentId) public view returns (TransactionStatus) {
    return transactionStatuses[paymentId];
}
```

## Security Features

* **Reentrancy Protection**: Uses OpenZeppelin's ReentrancyGuard
* **Access Control**: Implements role-based access control
* **MEV Protection**: Dynamic timing and trusted relayer system
* **Event Emissions**: Comprehensive transaction tracking

## Testing

```bash
# Run tests
npx hardhat test
```

## Contributing

Contributions are welcome! Please submit pull requests with:
1. Clear documentation of changes
2. Updated tests
3. Security considerations

## License

MIT License

Copyright (c) 2025 DimensionlessDevelopments

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
