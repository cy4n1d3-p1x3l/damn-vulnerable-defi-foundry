# Damn Vulnerable DeFi - Foundry Version ⚒️

My Solution for the famous damn-defi problems in foundry.

[![Twitter Follow](https://img.shields.io/twitter/follow/0xcyanide?label=Follow%20me%20%400xcyanide&style=social)](https://twitter.com/0xcyanide)

Visit [damnvulnerabledefi.xyz](https://damnvulnerabledefi.xyz)

### Acknowledgement
*Big thanks to [Tincho](https://twitter.com/tinchoabbate) who created the [first version of this game](https://github.com/tinchoabbate/damn-vulnerable-defi/tree/v2.0.0) and to all the fellows behind the [Foundry Framework](https://github.com/gakonst/foundry/graphs/contributors) and also [Nicolás](https://github.com/nicolasgarcia214/damn-vulnerable-defi-foundry) from whom i cloned the repo for the foundry version*

Damn Vulnerable DeFi is the wargame to learn offensive security of DeFi smart contracts.

Throughout numerous challenges you will build the skills to become a bug hunter or security auditor in the space. 🕵️‍♂️

## How To play 🕹️

1.  **Install Foundry**

First run the command below to get foundryup, the Foundry toolchain installer:

``` bash
curl -L https://foundry.paradigm.xyz | bash
```

Then, in a new terminal session or after reloading your PATH, run it to get the latest forge and cast binaries:

``` console
foundryup
```

2. **Clone This Repo and install dependencies**
```bash 
git clone https://github.com/nicolasgarcia214/damn-vulnerable-defi-foundry.git
cd damn-vulnerable-defi-foundry
forge install
```

3. **Run your exploit for a challenge**

```console
make [CONTRACT_LEVEL_NAME]
```
which essentially the command

```bash
forge test --match-contract [LEVEL_NAME] 
```

If the challenge is executed successfully, you've passed!🙌🙌

## Solutions

You can view my solutions in the respective test folders' Readme files.