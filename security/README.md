# Security

[Reentrancy attack](https://solidity-by-example.org/hacks/re-entrancy/)
  fallback()
  - update state variables before make any external calls
  - use ReentrancyGuard

[Forcefully Send Ether with selfdestruct](https://solidity-by-example.org/hacks/self-destruct/)
  - Don't rely on address(this).balance
  
