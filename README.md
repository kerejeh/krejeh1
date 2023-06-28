Open : https://remix.ethereum.org 
Create New File and Copy This Script And Paste To Your File

``` // SPDX-License-Identifier: MIT
pragma solidity ^0.8.0;

contract Register {
    string public github;
    address public owner;
    
    struct Referral {
        address referralAddress;
        string referralString;
    }
    
    Referral[] public referrals;
    
    constructor() {
        github = "ganti_pake_username_github_kalian";
        owner = “ganti_pake_address_kalian”;
    }
    
    function addReferral(address _referralAddress, string memory _referralString) external {
        require(msg.sender == owner, "Only the owner can add referrals.");
        referrals.push(Referral(_referralAddress, _referralString));
    }
    
    function totalReferrals() public view returns (uint256) {
        return referrals.length;
    }
} ```

Change The Github Name With Your Github Name 
And Address With Your Address 
Clikc Compile
after that click Deploy Change ENVIRONMENT with Injected Provider - MetaMask and click deploy 
