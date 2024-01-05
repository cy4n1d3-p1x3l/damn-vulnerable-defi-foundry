# Challenge #4 - Side entrance
A surprisingly simple lending pool allows anyone to deposit ETH, and withdraw it at any point in time.

This very simple lending pool has 1000 ETH in balance already, and is offering free flash loans using the deposited ETH to promote their system.

You must take all ETH from the lending pool.

[See the contracts](https://github.com/nicolasgarcia214/damn-vulnerable-defi-foundry/tree/master/src/Contracts/side-entrance)
<br/>
[Complete the challenge](https://github.com/nicolasgarcia214/damn-vulnerable-defi-foundry/blob/master/test/Levels/side-entrance/SideEntrance.t.sol)

## Solution

The vulnerability lies in the fact that the Lending Pool will consider the loan repaid if we just deposit the amount using the deposit function. And so we execute the [attack](../../../src/Contracts/side-entrance/Exploit.sol#L13) function which takes a flash loan and deposits it back. It then withdraws the amount and transfers it back to us. Hence completing the exploi.