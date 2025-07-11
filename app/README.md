# Cairn - Front End App

![header](/assets/header.png)

## Live demo

Visit: https://octopus-app-5rjoy.ondigitalocean.app/ <br>


> See [Quick Start](#quick-start) below to help you get started.
<br>

![Cairn Front End App](public/scientistImage.png)



## Overview

## Key Technologies

- **w3up-client**: A library for working with IPFS-based storage services.
- **ethers**: A library for connecting to blockchain networks and enabling decentralized features.
- **React**: Provides a component-based architecture for building interactive UIs.
- **TypeScript**: Adds static typing to JavaScript, improving code quality and maintainability.
- **Vite**: Offers lightning-fast development server and optimized production builds.
- **Tailwind CSS**: Enables rapid UI development with utility classes.


## Features

- **Decentralized Storage**: Upload and retrieve files using IPFS.
- **Blockchain Integration**: Interact with smart contracts on Filecoin Calibration test network.
- **Responsive Design**: Mobile-friendly layouts powered by Tailwind CSS.
- **Type-Safe Codebase**: Enhanced reliability and developer experience with TypeScript.

---

## Usage 
- Register project:
    - Use the `useRegisterProject` hook to register a new project with a name and description.

## Getting Started

1. **Install dependencies**:
    ```bash
    npm install
    ```
2. **Create a `.env` file** in the root directory and add your environment variables:
    ```env
    VITE_AGENT_KEY=xxxxx
    VITE_PROOF=xxxxx
    ```
    Replace `xxxxx` with your actual values. To see how to get these values, refer to the [w3up-client docs](https://docs.storacha.network/)
2. **Run the development server**:
    ```bash
    npm run dev
    ```
3. **Build for production**:
    ```bash
    npm run build
    ```

## Learn More

- [W3up-client](https://docs.storacha.network/)
- [Ethers Docs](https://docs.ethers.org/v5/)
- [React Documentation](https://react.dev/)
- [TypeScript Handbook](https://www.typescriptlang.org/docs/)
- [Vite Guide](https://vitejs.dev/guide/)
- [Tailwind CSS Docs](https://tailwindcss.com/docs)
  
---

###  Quick Start
This is meant to be a quick start guide for users who want to quickly try out the Cairn protocol and platform.

#### 🔵 Wallet Setup
1. **Install MetaMask**:  
   Download and install the [MetaMask browser extension](https://metamask.io/).
2. **Create a Wallet**:
    Follow the instructions to create a new wallet. Make sure to securely store your seed phrase.
3. **Connect to Filecoin Calibration Testnet**:
    - **Cairn app should prompt the user with correct chain data**
    - If not, you can manually add the network:
      - Open MetaMask and click on the network dropdown.
      - Select "Add Network" and enter the following details:
        - **Network Name**: Filecoin Calibration Testnet
        - **New RPC URL**: https://rpc.ankr.com/filecoin_testnet
        - Other data should be filled automatically.

#### 🔵 Getting Testnet tFIL and USDFC
1. **Get tFIL**:  
   Use the [Filecoin Calibration Faucet](https://faucet.calibnet.chainsafe-fil.io/) to request testnet FIL (tFIL) for gas fees.\
   Enter your wallet address in the input field and send 100 tFIL to your wallet.
3. **Get USDFC**:
    Use the [USDFC Faucet](https://forest-explorer.chainsafe.dev/faucet/calibnet_usdfc) to request USDFC tokens for funding projects.

#### 🔵 Choosing a role
To switch between Scientist and Funder dashboard head over to the top right corner, where you see your profile and wallet address. 

#### 🔵 Register a New Project - Scientist role
Before you can register a new project, you need to submit a minimum of one Proof of Reproducibility (PoR) and that PoR needs to get verified on-chain. The demo app is currently running on the testnet and it takes ~2 minutes to do that:
 1. Click on the button or card "New project" and fill out the form. In this step you must also define your Funding Goal.
 2. Click on the button "Create Project". This starts a 3 step process of the project being created on-chain:
  - Confirm the transaction request in the Metamask wallet. The app is uploading the project metadata to IPFS. Then it starts minting the Hypercert.
  - Confirm the withdrawal request for the Hypercert approval.
  - Confirm the transaction request. The app is connecting the project and Hypercert token ID.
    
 #### 🔵 Submitting Record Outputs - Scientist role
 1. Click on "View Project" and head over to Research Outputs section and add fill out the Output fields
 2. Confirm the transaction request in Metamask to record the outputs on-chain. 

#### 🔵 Submiting a Proof of Reproducibility - Scientist role
To submit a PoR, you need to select a project with a registered output. Click On "Submit Reproducibility", provide the requested repruducibility proof and submit.
The verification of the PoR for this demo takes about 5 minutes. In the meantime, other users can dispute on your PoR if they find it not suitable. The timespan of this action would normally be a couple of days.

#### 🔵 Fund a project - Funder role
To fund a project you simply select a project in the Discovery tab, where you can see the funding amount and the impact score of each project. 
For now the funding is only possible for the whole amount of the project's funding goal. Just clisk on the button "Fund" and you will see the project in your portfolio.



