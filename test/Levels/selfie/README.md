# Challenge #6 - Selfie
A new cool lending pool has launched! It's now offering flash loans of DVT tokens.

Wow, and it even includes a really fancy governance mechanism to control it.

What could go wrong, right ?

You start with no DVT tokens in balance, and the pool has 1.5 million. Your objective: take them all.

[See the contracts](https://github.com/nicolasgarcia214/damn-vulnerable-defi-foundry/tree/master/src/Contracts/selfie)
<br/>
[Complete the challenge](https://github.com/nicolasgarcia214/damn-vulnerable-defi-foundry/blob/master/test/Levels/selfie/Selfie.t.sol)

## Solution 

The vunlnerability lies in the fact that we can take a [snapshot](../../../src/Contracts/DamnValuableTokenSnapshot.sol#L17) anytime and has no restriction check and the governance contract will then consider that snapshot to check if we have enough votes or not [here](../../../src/Contracts/selfie/SimpleGovernance.sol#L92).

We write the [Exploit](../../../src/Contracts/selfie/Exploit.sol) contract. It takes a flash loan and then we take a snapshot of the balances at that time which gives us more than half the total supply and it helps us to queue our action of draining the contract fully. We then [wait](./Selfie.t.sol#L48) for 2 days and execute the action and take control of out funds.
