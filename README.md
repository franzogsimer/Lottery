# Lottery
#### The process flow diagram are made from book of "Building Games With Ethereum Smart Contracts" and converted or redesigned in Hyperledger Fabric. 

## Simple Lottery
This lottery is non-recurring and has only one winner.

## Recurring Lottery
This lottery is more realistic lottery contract that can be deployed to mainnet. The new lottery will occur in rounds so that a new prize pool is started every time the old one closes. It will also allow users to purchase multiple tickets in one transaction instead of just one and add a couple of security improvements.

## RNG Lottery
RNG lottery is to use a commit-reveal sequence to create a verifiably random number. Every buyer submits a commitment hash when they buy ticket. The commitment is generated by hashing together the user’s address and a secret number known only to the user. When the ticketing period is over, there is a reveal period during which each player must reveal the secret number used to generate their commitment hash. The secret number is hashed on-chain with the player’s address, and this hash must match the commitment submitted with the ticket. Players who don’t reveal their numbers during the reveal period are dropped from the lottery. The secret numbers are hashed together to generate the random seed for picking a winner.

## Powerball Lottery
In Powerball, the user picks six numbers per ticket. The first five numbers are standard numbers from 1–69, and the sixth number is a special Powerball number from 1–26 that offers extra rewards. Every three or four days, a drawing is held, and a winning ticket consisting of five standard numbers and a Powerball number is picked. Prizes are paid out based on the number of winning numbers matched on your ticket.
