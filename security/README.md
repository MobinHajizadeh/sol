# Security

## Attacks
[Reentrancy attack](https://solidity-by-example.org/hacks/re-entrancy/)
  fallback()
  - update state variables before make any external calls
  - use ReentrancyGuard

[Forcefully Send Ether with selfdestruct](https://solidity-by-example.org/hacks/self-destruct/)
  - Don't rely on address(this).balance
  
[Unsafe Delegatecall](https://solidity-by-example.org/hacks/delegatecall/)

[DOS](https://solidity-by-example.org/hacks/denial-of-service/)

## Tools
[Tenderly](https://tenderly.co)
  - alert
  - simulation 
  - debug

[Flashbots](https://docs.flashbots.net/)
  - sandwich attacks
