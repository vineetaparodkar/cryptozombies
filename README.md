# Cryptozombies Hardhat Project

This project contains cryptozombies challenges from `https://cryptozombies.io/en/lesson/1`


# Cryptozombies Overview

1. Lesson 1

-  To build a "Zombie Factory" to build an army of zombies.

    1. Our factory will maintain a database of all zombies in our army ==>public array of Zombie structs
    2. Our factory will have a function for creating new zombies ==>a public function named createRandomZombie
    3. Each zombie will have a random and unique appearance ==> _generateRandomDna


2. Lesson 2

- zombie feeding: When a zombie feeds, it infects the host with a virus. The virus then turns the host into a new zombie that joins your army. The new zombie's DNA will be calculated from the previous zombie's DNA and the host's DNA.

    1. Create a multiplayer game ==> Create a mapping called zombieToOwner,ownerZombieCount

    2. implementing the functionality for our zombies to feed and multiply. ==> Create a function called feedAndMultiply. Define an interface called KittyInterface. function feedOnKitty

3. Lesson 4

- Let's say our game has a feature where users can pay ETH to level up their zombies. The ETH will get stored in the contract, which you own — this a simple example of how you could make money on your games! 

    1. create level up functionality to level up by paying eth
    
    2. withdraw eth from contract to collect fees

    3. Let's implement a random number function we can use to determine the outcome of our battles,we can use it in our zombie battles to calculate the outcome. ==> random function with hash, time,nonce

    Our zombie battles will work as follows:

    You choose one of your zombies, and choose an opponent's zombie to attack.
    If you're the attacking zombie, you will have a 70% chance of winning. The defending zombie will have a 30% chance of winning.
    All zombies (attacking and defending) will have a winCount and a lossCount that will increment depending on the outcome of the battle.
    If the attacking zombie wins, it levels up and spawns a new zombie.
    If it loses, nothing happens (except its lossCount incrementing).
    Whether it wins or loses, the attacking zombie's cooldown time will be triggered.

    Create an if statement that checks if rand is less than or equal to attackVictoryProbability.

    If this condition is true, our zombie wins! So:

    a. Increment myZombie's winCount.

    b. Increment myZombie's level. (Level up!!!!!!!)

    c. Increment enemyZombie's lossCount. (Loser!!!!!! 😫 😫 😫)

    d. Run the feedAndMultiply function

    4. Run the _triggerCooldown function on myZombie. This way the zombie can only attack once per day. 

4. Lesson5: NFT Collectible 

- Implement a zombie owner,balanceof,transfer functionality to update mapping


## Setup

- Add Ropsten or Polygon RPC URL's,deployer account private key in .env file.

- Compile Solidity Cryptozombies contract with below command

    `npx hardhat compile`

- Deploy cryptozombies smart contract with below command

    `node scripts/deploy.js`
