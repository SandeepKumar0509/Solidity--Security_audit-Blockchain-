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
   ```
  Run this Contract in the docker image we just pull:
  ```
  $ docker run -it -v $PWD:/data devopstestlab/solgraph
  ```
  View the image using:
  - For Ubuntu/Linux
    ```
    $ xdg-open MyContract.sol.png
    ```
  - Wsl Ubuntu
 
    ```
    $ eog MyContract.sol.png
    ```

![image](https://github.com/SandeepKumar0509/Solidity--Security_audit-Blockchain-/assets/143065262/427e970a-5779-4775-a49b-b76c13dbc337)

