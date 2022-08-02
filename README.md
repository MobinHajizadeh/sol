# solidity-gas

Transaction fee = gas used by the transaction * gas price

Transfer ether: 21,000 gas

Every Transaction: 21,000 gas + x

Ex.
| Operation | Gas cost | Gas price(gwei) | Transaction fee(ether) |
| :---: | :---: | :---: | :---: |
| ETH transfer | 21,000 | 50 | 0.00105 |

=> payable functions costs less gas than non-payable functions.

=> unchecked costs less gas.

=> The higher the number of optimization, the more deployment gas, 
   but less gas is consumed to interact with the contract.
   ex. Uniswap optimization number = 1,000,000
