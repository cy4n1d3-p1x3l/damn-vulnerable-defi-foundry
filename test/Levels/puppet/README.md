# Challenge #8 - Puppet
There's a huge lending pool borrowing Damn Valuable Tokens (DVTs), where you first need to deposit twice the borrow amount in ETH as collateral. The pool currently has 100000 DVTs in liquidity.

There's a DVT market opened in an [Uniswap v1 exchange](https://docs.uniswap.org/contracts/v1/overview), currently with 10 ETH and 10 DVT in liquidity.

Starting with 25 ETH and 1000 DVTs in balance, you must steal all tokens from the lending pool.

[See the contracts](https://github.com/nicolasgarcia214/damn-vulnerable-defi-foundry/tree/master/src/Contracts/puppet)
<br/>
[Complete the challenge](https://github.com/nicolasgarcia214/damn-vulnerable-defi-foundry/blob/master/test/Levels/puppet/Puppet.t.sol)

## Solution 

Firstly there is some issue with foundry latest version so i had to use this sepcific commit and it worked ```94777647f6ea5d34572a1b15c9b57e35b8c77b41```.
We can just manipulate the exchange rate and drain the contract of all the dvt tokens. You can see the exploit [here](./Puppet.t.sol/#L102).  