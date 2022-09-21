# Gas

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
- setting sorage from 0 to non-zero: 22,100 [ 20,000 + 2,100(cold storage) ]
- setting sorage from non-zero to non-zero: 5,000 [ 2,900 + 2,100(cold storage) ]
- setting sorage from non-zero to 0: refund (cost between 200 and 5000 gas)
- deleting an array (or setting many values to 0) can be expensive.
- setting one variable to 0 is ok. setting several variables to 0 is like doing several non-zero to non-zero operations.
- counting down is more efficient than counting up.
- pay additional 2,100 gas if it is the first time accessing a variable in a transaction. (cold storage)
- pay additional 100 gas if the variable has already been touched.

=> memory is more expensive than calldata. | calldata can not be changed.

=> compiler sorts functions (function selectors) in hexadecimal order.
   if you have a function that is very gas sensitive, you should try to make sure that it's function selector is near the top.
   function selector = first 4 bytes of the keccak256 of the function name.

=> use <, > or == instead of <= or >=

=> use shift instead of multily by 2k or divide by 2k.
   Ex. 
      n * 2 = n << 1
      n / 2 = n >> 1

=> use short circuiting.

=> private, internal are cheaper than public, external.

=> errors are cheaper than requires(store string onchain).
