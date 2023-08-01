# FundMe - Smart Contract for Crowdfunding on Ethereum


## Introduction

Welcome to the "FundMe" project! This repository contains the Solidity smart contract and the "PriceConverter" library for enabling crowdfunding campaigns on the Ethereum blockchain. The project leverages Chainlink's decentralized oracle network through the "PriceConverter" library to determine the equivalent USD value of Ether (ETH) contributions made by backers. This README provides an overview of the contract and its functionalities.

## Table of Contents

- [FundMe - Smart Contract for Crowdfunding on Ethereum](#fundme---smart-contract-for-crowdfunding-on-ethereum)
  - [Introduction](#introduction)
  - [Table of Contents](#table-of-contents)
  - [Contract Overview](#contract-overview)
  - [PriceConverter Library](#priceconverter-library)
  - [Usage](#usage)
  - [Contributing](#contributing)
  - [License](#license)

## Contract Overview

The "FundMe" contract facilitates crowdfunding by allowing users to contribute Ether to creative projects and receive funding for their initiatives. It includes the following essential features:

- **Contributions**: Users can make contributions to creative projects by sending Ether to the contract.
- **Minimum Contribution**: To participate, backers must contribute an amount equal to or greater than the minimum specified USD value (MINIMUM_USD), as determined by the "PriceConverter" library.
- **Project Tracking**: The contract keeps track of the amount funded by each contributor and maintains an array of funder addresses.
- **Withdrawal**: The contract owner can withdraw the total balance of the contract, distributing the funds to all backers who contributed to the projects.

## PriceConverter Library

The "PriceConverter" library provides functionalities to convert Ether amounts to their equivalent USD values. It utilizes the Chainlink decentralized oracle to fetch the latest ETH/USD price and then calculates the conversion rate for a given Ether amount.

## Usage

1. **Contract Deployment**: To use the "FundMe" contract, deploy it to the Ethereum blockchain, along with the "PriceConverter" library.

2. **Minimum Contribution Setting**: Set the minimum contribution value (MINIMUM_USD) in the contract. This value represents the minimum USD equivalent amount required for backers to contribute.

3. **Funding**: Backers can interact with the contract by calling the "fund()" function and sending Ether to contribute to creative projects. The contract will validate whether the contribution meets the minimum USD requirement based on the latest ETH/USD rate obtained through the "PriceConverter" library.

4. **Withdrawal**: The contract owner can execute the "cheaperWithdraw()" function to distribute funds to all backers. The contract will set the contribution amount of each funder to zero and then transfer the contract balance to the owner.

## Contributing

We welcome contributions from the community to improve the "FundMe" project. If you have ideas for new features or bug fixes, please follow these steps:

1. Fork the repository to your GitHub account.
2. Create a new branch for your feature/bug fix: `git checkout -b feature/your-feature-name` or `git checkout -b bugfix/issue-number`.
3. Commit your changes and push the branch to your forked repository.
4. Submit a pull request detailing your changes.

## License

This project is licensed under the [MIT License](https://opensource.org/licenses/MIT). See the LICENSE file for more information.

---
