# <h1 align="center"> Forge Template </h1>

**Template repository for getting started quickly with Foundry projects**

![Github Actions](https://github.com/foundry-rs/forge-template/workflows/CI/badge.svg)

## Getting Started

Click "Use this template" on [GitHub](https://github.com/foundry-rs/forge-template) to create a new repository with this repo as the initial state.

Or, if your repo already exists, run:
```sh
forge init
forge build
forge test
```

## Writing your first test

All you need is to `import forge-std/Test.sol` and then inherit it from your test contract. Forge-std's Test contract comes with a pre-instatiated [cheatcodes environment](https://book.getfoundry.sh/cheatcodes/), the `vm`. It also has support for [ds-test](https://book.getfoundry.sh/reference/ds-test.html)-style logs and assertions. Finally, it supports Hardhat's [console.log](https://github.com/brockelmore/forge-std/blob/master/src/console.sol). The logging functionalities require `-vvvv`.

```solidity
pragma solidity 0.8.10;

import "forge-std/Test.sol";

contract ContractTest is Test {
    function testExample() public {
        vm.roll(100);
        console.log(1);
        emit log("hi");
        assertTrue(true);
    }
}
```

## Development

This project uses [Foundry](https://getfoundry.sh). See the [book](https://book.getfoundry.sh/getting-started/installation.html) for instructions on how to install and use Foundry.


Analysing contracts...
Running tests...
| File                         | % Lines          | % Statements     | % Branches     | % Funcs        |
|------------------------------|------------------|------------------|----------------|----------------|
| src/libraries/Math.sol       | 88.89% (8/9)     | 90.00% (9/10)    | 75.00% (3/4)   | 100.00% (2/2)  |
| src/libraries/UQ112x112.sol  | 0.00% (0/2)      | 0.00% (0/2)      | 100.00% (0/0)  | 0.00% (0/2)    |
| src/uniswapV2Factory.sol     | 100.00% (12/12)  | 100.00% (17/17)  | 100.00% (6/6)  | 100.00% (1/1)  |
| src/uniswapV2Library.sol     | 100.00% (34/34)  | 96.61% (57/59)   | 87.50% (14/16) | 100.00% (8/8)  |
| src/uniswapV2Pair.sol        | 95.52% (64/67)   | 95.56% (86/90)   | 82.14% (23/28) | 100.00% (8/8)  |
| src/uniswapV2Router.sol      | 93.02% (40/43)   | 94.83% (55/58)   | 77.27% (17/22) | 100.00% (7/7)  |
| test/mocks/ERC20Mintable.sol | 0.00% (0/1)      | 0.00% (0/1)      | 100.00% (0/0)  | 0.00% (0/1)    |
| test/uniswapV2Pair.sol       | 93.33% (14/15)   | 89.47% (17/19)   | 66.67% (4/6)   | 100.00% (4/4)  |
| Total                        | 93.99% (172/183) | 94.14% (241/256) | 81.71% (67/82) | 90.91% (30/33) |