# Surya 
Surya is an utility tool for smart contract systems. 
It provides a number of visual outputs and information about the contracts' structure
It also supports querying the function call graph in multiple ways to aid in the manual inspection of contracts.

# Surya
Surya is a tool for smart contract visualization and analysis for Ethereum.
It provides insights into the structure of Solidity smart contracts by generating
interactive diagrams and graphs, allowing developers and auditors to better understand 
the relationships between different parts of the contract code.

# How to Install Surya
Step-1: Install Node.js and npm if not installed.
```
sudo apt update
sudo apt install nodejs npm
```
Step-2: After downloading nodejs npm ,install graphivz, in order to view graph output.
```
sudo apt install graphviz
```
To verify if graphivz is installed use this command :
```
dot -V
```
Step-3: install Surya:
```
sudo npm install -g surya
```
Step-4: To verify if Surya is installed or not use:
```
surya --version
```
