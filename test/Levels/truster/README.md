# Challenge #3 - Truster
More and more lending pools are offering flash loans. In this case, a new pool has launched that is offering flash loans of DVT tokens for free.

Currently the pool has 1 million DVT tokens in balance. And you have nothing.

But don't worry, you might be able to take them all from the pool. In a single transaction.

[See the contracts](https://github.com/nicolasgarcia214/damn-vulnerable-defi-foundry/tree/master/src/Contracts/truster)
<br/>
[Complete the challenge](https://github.com/nicolasgarcia214/damn-vulnerable-defi-foundry/blob/master/test/Levels/truster/Truster.t.sol)

## Solution

The *vulnerability* lied in this line [here](../../../src/Contracts/truster/TrusterLenderPool.sol#L32). It allowed us to call have any contract function called. Now any function call will be passed from the context of the LenderPool and so we can exploit it easily [here](../../Levels/truster/Truster.t.sol#L41). We call the *approve* function of the dvt erc20 token which helps us to transfer these tokens to us afterwards and drain the contract. We used 0 as the amount beacuse now we won't have to return any eth back.