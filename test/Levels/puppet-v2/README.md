# Challenge #9 - Puppet V2
The developers of the [last lending pool](https://github.com/nicolasgarcia214/damn-vulnerable-defi-foundry/tree/master/test/Levels/puppet) are saying that they've learned the lesson. And just released a new version!

Now they're using a [Uniswap v2 exchange](https://docs.uniswap.org/protocol/V2/introduction) as a price oracle, along with the recommended utility libraries. That should be enough.

You start with 20 ETH and 10000 DVT tokens in balance. The new lending pool has a million DVT tokens in balance. You know what to do ;)

[See the contracts](https://github.com/nicolasgarcia214/damn-vulnerable-defi-foundry/tree/master/src/Contracts/puppet-v2)
<br/>
[Complete the challenge](https://github.com/nicolasgarcia214/damn-vulnerable-defi-foundry/blob/master/test/Levels/puppet-v2/PuppetV2.t.sol)

### Solution
It was also an easy level, learnt the working of uniswapV2. Since the liquidity is pretty low, we can just swap the tokens giving us more tokens to start with and also lowering the price due to the hyperbolic price deterministic function.
See my solution [here](../../../test/Levels/puppet-v2/PuppetV2.t.sol#L98)
