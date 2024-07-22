# Lottery

# Lottery Smart Contract

This repository contains a Solidity smart contract for a simple lottery system on the Ethereum blockchain. 

## Contract Details

### Entities
- **Manager**: The person who deploys the contract and manages the lottery.
- **Players**: Participants who enter the lottery by paying 1 ether.
- **Winner**: The player who wins the lottery and receives the entire balance of the contract.

### Functions
- `constructor()`: Sets the manager to the address that deploys the contract.
- `participate()`: Allows players to enter the lottery by sending exactly 1 ether.
- `getBalance()`: Returns the current balance of the contract. Only callable by the manager.
- `random()`: Generates a pseudo-random number used to pick the winner.
- `pickWinner()`: Selects a random winner from the players, transfers the contract balance to the winner, and resets the players array. Can only be called by the manager and requires at least 3 players to have participated.


####Usage
1.Deploy the Contract: The person deploying the contract becomes the manager.
2.Participate in the Lottery: Players can enter the lottery by calling the participate function and sending exactly 1 ether.
3.Check Balance: The manager can check the contract's balance by calling the getBalance function.
4.Pick a Winner: Once there are at least 3 players, the manager can call the pickWinner function to randomly select a winner and transfer the contract balance to them.
