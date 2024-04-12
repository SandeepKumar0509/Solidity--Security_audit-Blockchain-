# Solidity-Security-Audit

## Security Audit for Solidity
- **Slither**
- **Solgraph**

## Slither 
```
$ sudo apt install software-properties-common

$ sudo add-apt-repository ppa:ethereum/ethereum

$ sudo apt install solc

$ pip3 install solc-select

**Using pip**

$ pip3 install slither-analyzer

**Using GitHub**

$ git clone <https://github.com/crytic/slither.git> && cd slither

$ python3 setup.py install

**Using Docker**

$ docker pull trailofbits/eth-security-toolbox
```
#### Make a file named contractname.sol
```
touch contractname.sol
```
```
nano
```
- Write a contract ( you can find it on github)
```
pragma solidity ^0.4.15;

contract CrowdFundBad {
  address[] private refundAddresses;
  mapping(address => uint) public refundAmount;

  function refundDos() public {
    for(uint i; i < refundAddresses.length; i++) {
      require(refundAddresses[i].transfer(refundAmount[refundAddresses[i]]));
    }
  }
}

contract CrowdFundPull {
  address[] private refundAddresses;
  mapping(address => uint) public refundAmount;

  function withdraw() external {
    uint refund = refundAmount[msg.sender];
    refundAmount[msg.sender] = 0;
    msg.sender.transfer(refund);
  }
}


//This is safe against the list length causing out of gas issues
//but is not safe against the payee causing the execution to revert
contract CrowdFundSafe {
  address[] private refundAddresses;
  mapping(address => uint) public refundAmount;
  uint256 nextIdx;
  
  function refundSafe() public {
    uint256 i = nextIdx;
    while(i < refundAddresses.length && msg.gas > 200000) {
      refundAddresses[i].transfer(refundAmount[i]);
      i++;
    }
    nextIdx = i;
  }
}
```

# after that make a Local copy of a contract file using these commands :-


 
```
$ solc-select use Solidity-compilerversion(like 0.5.15)

$ slither filename.sol
```

 
  - For Ubuntu/Linux
    ``` 
    $ xdg-open MyContract.sol.png
    ```
  - Wsl Ubuntu
    ```
    $ eog MyContract.sol.png
    
    ![320475753-d4de0fa4-815c-4458-b617-a195e225606f](https://github.com/SandeepKumar0509/Solidity--Security_audit-Blockchain-/assets/143065262/6d53c415-139d-4f70-8e72-ee0abc7d2089)
