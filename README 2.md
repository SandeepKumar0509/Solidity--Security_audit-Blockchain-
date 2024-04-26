   # Decentralized applications (dApps) are one of the most promising applications of blockchain technology. They open up new Possibilities for consumer and business-focused products with never-before-seen capabilities.

 #   Prerequisite  
 Let us ensure we have Node/NPM installed on our PC. If we don't have it installed, head over here for a guide.

 # Project Setup and Installation
 ##  Let's navigate to the terminal. We'll need to cd into any directory of our choice and then run the following commands:
 ``` 
 mkdir newsfeed-be
cd newsfeed-be
npm init -y
npm install --save-dev hardhat 
```

Let's get a sample project by running the command below:
```

 npx hardhat
```
 ## We'll go with the following options:

    A sample project.

    Accept all other requests.

Installing hardhat-waffle and hardhat-ethers is required for the sample project.

Just in case it didn't install automatically, we will install this other requirement with the following command:
```
npm install --save-dev @nomiclabs/hardhat-waffle ethereum-waffle chai @nomiclabs/hardhat-ethers ethers @openzeppelin/contracts
```

Next, we will install @openzeppelin/contracts for the counter we will use later in this .
```
npm i @openzeppelin/contracts
```

To make sure everything is working, let us run the command below.
```
npx hardhat test
```
