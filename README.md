# DeFI-Brownie

This is a repo to build your own full stack defi staking application for yield farming, borrowing and lending, or any other project you can think of. It allows you to:

stakeTokens: Add any approved token to the farming contract for yeild farming, collateral, or whatever you want to do.
unStakeTokens: Remove your tokens from the contract.
getUserTotalValue: Get the total value that users have supplied based on calculations from the Chainlink Price Feeds.
issueTokens: Issue a reward to the users staking on your platform!

As a result of the marge Rinkeby, Kovan, Ropsten are deprecated 
so we are using GOERLI

Prerequisites

Please install or have installed the following:

nodejs and npm
python

Installation
Install Brownie, if you haven't already. Here is a way to install brownie.
pip install --user pipx
pipx ensurepath
# restart your terminal
pipx install eth-brownie
Or if you can't get pipx to work, via pip (it's recommended to use pipx)

pip install eth-brownie
Clone this repo
git clone https://github.com/max-clinch/DeFI-Brownie.git
cd DeFI-Brownie
Install ganache-cli
npm install -g ganache-cli
If you want to be able to deploy to testnets, do the following.

Set your environment variables
Set your WEB3_INFURA_PROJECT_ID, and PRIVATE_KEY environment variables.

You can get a WEB3_INFURA_PROJECT_ID by getting a free trial of Infura. At the moment, it does need to be infura with brownie. You can find your PRIVATE_KEY from your ethereum wallet like metamask.

You'll also want an Etherscan API Key to verify your smart contracts.

You can add your environment variables to the .env file:

export WEB3_INFURA_PROJECT_ID=<PROJECT_ID>
export PRIVATE_KEY=<PRIVATE_KEY>
export ETHERSCAN_TOKEN=<YOUR_TOKEN>
DO NOT SEND YOUR KEYS TO GITHUB If you do that, people can steal all your funds. Ideally use an account with no real money in it.

Useage
Scripts
brownie run scripts/deploy.py
This will deploy the contracts, depoly some mock Chainlink contracts for you to interact with.

brownie run scripts/deploy.py --network goerli
