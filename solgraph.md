## Solgraph (solc converts from a high-level solidity language into Ethereum Virtual Machine (EVM) bytecode so that it can be executed on the blockchain by EVM)
#### Pre-requisite 
- Install Docker
- Pull devopstestlab/solgraph:
  ```
  $ docker pull devopstestlab/solgraph
  ```
  #### Create the Smart Contract in Solidity
  ```
  $ sudo mkdir data
  $ cd data
  $ sudo vi MyContract.sol
   Run this Contract in the docker image we just pull:
  ```
  $ docker run -it -v $PWD:/data devopstestlab/solgraph
  ```
  View the image using:
  ![image](https://github.com/SandeepKumar0509/Solidity--Security_audit-Blockchain-/assets/143065262/53938d26-49ec-4402-93d7-16c8fdd684b9)

