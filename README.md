# <h1 align="center"> Spark Template </h1>

**Template repository for getting started quickly with Foxar projects**

## Getting Started

Click "Use this template" on [GitHub](https://github.com/bchainhub/spark-template) to create a new repository with this repo as the initial state.

Or, if your repo already exists, run:
```sh
spark init
spark build
spark test
```

## Writing your first test

All you need is to `import spark-std/Test.sol` and then inherit it from your test contract. Spark-std's Test contract comes with a pre-instatiated cheatcodes environment, the `vm`. It also has support for ds-test-style logs and assertions. Finally, it supports Hardhat's console.log. The logging functionalities require `-vvvv`.

```solidity
pragma solidity ^1.1.0;

import "spark-std/Test.sol";

contract ContractTest is Test {
    function testExample() public {
        vm.roll(100);
        console.log(1);
        emit log("hi");
        assertTrue(true);
    }
}
```
