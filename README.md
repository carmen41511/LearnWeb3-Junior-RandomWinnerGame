# RandomWinnerGame
This smart contract allows users to play a lottery game on Polygon Mumbai Testnet where a random winner is selected using Chainlink VRF.

## How It Works
1. The contract owner starts a new game by calling the startGame function, specifying the maximum number of players and entry fee.
2. Players call the joinGame function, sending the entry fee amount of MATIC. Their address is added to the players array.
3. Once the maximum number of players is reached, getRandomWinner is called to request randomness from Chainlink VRF.
4. The VRFCoordinator fulfills the request, returning a random number. This number is used to select a random winner from the players array.
5. The contract balance is sent to the winner, and the gameStarted flag is reset to allow a new game.

## Deployment
The contract is deployed to the Mumbai testnet using Hardhat and verified on Polygonscan for transparency. It integrates the latest Chainlink VRF and ERC-20 abstractions.

## Tools Used
- Solidity
- Hardhat
- OpenZeppelin
- Chainlink VRF
- Polygon Mumbai Testnet
- Polygonscan
