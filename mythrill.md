# What is Mythrill ?
1 -Mythril is a security analysis tool for Ethereum smart contracts.
2 -Mythril detects a range of security issues, including integer underflows, owner-overwrite-to-Ether-withdrawal, and others.

# How to install Mythrill ?
Here  are the steps :-
1 - Check Whether the python and pip is installed or not

```
python --version
```
if not installed used these commands:-
```
sudo apt update
```
```
sudo apt install python3
```
install pip 
```
sudo apt install python3-pip
```
install mythril
```
pip3 install mythril
```
check and verify the installation 
```
mythril --version
```
  # now we have to run mythrill 
  create a file named mycontract.sol then use  nano contract.sol
  ```
pragma solidity ^0.4.15;

contract Missing{
    address private owner;

    modifier onlyowner {
        require(msg.sender==owner);
        _;
    }

    // The name of the constructor should be Missing
    // Anyone can call the IamMissing once the contract is deployed
    function IamMissing()
        public 
    {
        owner = msg.sender;
    }

    function withdraw() 
        public 
        onlyowner
    {
       owner.transfer(this.balance);
    }
}
```
after that go to terminal and addd it 
```
myth analyze my_contract.sol
```
 # after that the output of this is here below 
![Screenshot (74)](https://github.com/SandeepKumar0509/Solidity--Security_audit-Blockchain-/assets/143065262/d57da844-22ab-4cd1-add2-de4b936c0975)
