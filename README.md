# Ethereum-DApp for a Car-Auction system

## Backend
The backend layer is represented by the auction.sol file which is the smart contract that manages the auction.
We used solidity to write our contract.
We'll consider the following auction design.

A vehicle's owner deploys the contract to the blockchain and becomes the auction owner. The auction is open immediately after the contract deployment, and, once the bidding period is over, the highest bidder wins the auction, and the other participants withdraw their bids. In this example, the bid will be cumulative, which means that if, for example, you bid 100 ETH, and then someone else bids 110 ETH, you can only send an additional 10.000000000000000001 ETH the next time to outbid them; your new bid is the sum of your two bids.

Furthermore, the auction owner can cancel the auction in exceptional cases, and must also be allowed, at the end of the auction, to withdraw the winning bid. The auction interaction flow is illustrated in the following diagram:

![ethereum-dapp-with-solidity-truffle4](https://user-images.githubusercontent.com/44893239/132295026-1cdb0a00-e51b-4167-ab16-68692587ffe5.jpg)

the Ethereum project provides us with the Remix web browser IDE (also known as Browser-Solidity), which is an online IDE that can be used to compile, deploy, and invoke smart contracts.
Once the deployment is successful, we'll get a form representing our contract methods and states' as shown here:

![ethereum-dapp-with-solidity-truffle10](https://user-images.githubusercontent.com/44893239/132295675-e1fb608b-b2dc-4e13-b3f9-6ac9a812357d.gif)

## Frontend
After a first validation of the auction contract using Remix in our previous recipe, it's time to move to the frontend and build a simple web interface that allows participants to interact with the auction.

![Screenshot (2)](https://user-images.githubusercontent.com/44893239/132295917-8d95c8e5-e438-46ab-84e4-02497b050714.png)

