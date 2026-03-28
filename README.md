# Faucet.sol
Base - Smart Contract Deployed by Remix Faucet.sol
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.20;

contract Faucet {
    function withdraw(uint _amount) public {
        require(_amount <= 0.1 ether, "Max 0.1 ETH");
        payable(msg.sender).transfer(_amount);
    }

    receive() external payable {}
}
