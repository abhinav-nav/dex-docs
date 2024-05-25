
# icp_dex: A Decentralized Exchange on the Internet Computer 

icp_dex is a decentralized exchange platform built on the Internet Computer Protocol (ICP). It enables secure and efficient trading of tokens, directly from your wallet.

## Table of Contents

- [Features](#features)
- [Getting Started](#getting-started)
    - [Prerequisites](#prerequisites)
    - [Installation](#installation)
    - [Running Locally](#running-locally)
- [Project Structure](#project-structure)
- [Frontend Development](#frontend-development)

## Features

* **Decentralized Trading:** Trade directly from your wallet, eliminating intermediaries.
* **Token Support:** Seamlessly trade a variety of tokens.
* **Fast and Secure:** Leverage the speed and security of the Internet Computer.
* **User-Friendly Interface:** An intuitive design for easy navigation and trading.

## Getting Started

### Prerequisites

* Node.js and npm (or yarn)
* DFX (The ICP development kit): Install instructions can be found [here](https://internetcomputer.org/docs/current/developer-docs/setup/install/index.html).

### Installation

1. Clone this repository: 
   ```bash
   git clone [url]


Navigate to the project directory:

Bash
cd icp_dex

Install dependencies:

Bash
npm install 

Running Locally
Start the local replica:

Bash
dfx start --background

Deploy canisters and generate Candid interface:

Bash
dfx deploy

Start the frontend development server:

Bash
npm start

Your application will be available at http://localhost:8080, proxying API requests to the replica at port 4943.

Project Structure
/src: Source code for your project's canisters (backend) and frontend.
dfx.json: Configuration file for DFX.
package.json: Lists project dependencies and scripts.

Frontend Development
The frontend development server can be started with npm start. This will start a server at http://localhost:8080, proxying API requests to the replica at port 4943.

Important Note: If hosting frontend code without DFX, adjust environment variables to prevent fetching the root key in production. You can do this by either:

Setting DFX_NETWORK to ic if using Webpack
Using your preferred method to replace process.env.DFX_NETWORK in the autogenerated declarations
Setting canisters -> {asset_canister_id} -> declarations -> env_override to a string in dfx.json
