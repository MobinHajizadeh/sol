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

Gas Costs:
- setting sorage from 0 to non-zero: 20,000
- setting sorage from non-zero to non-zero: 5,000
- setting sorage from non-zero to 0: refund

pay additional 2,100 gas if it is the first time accessing a variable in a transaction ( cold storage )
pay additional 100 gas if the variable has already been touched
