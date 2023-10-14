### 1]  What are the advantages and disadvantages of the 256 bit word length in the EVM

**=>  Advantages of 256-bit word length in the EVM:**

**i) Canhandle very large numbers.**
**ii) Enhanced security for smart contracts.**

**Disadvantages:**

**i) Increased gas costs.**

**ii) More storage and memory needed.**

**iii) Complex arithmetic operations.**


### 2]   What would happen if the implementation of a precompiled contract varied between Ethereum clients ?

 **=> Ifthe implementation of a precompiled contract varies between Ethereum clients, it can lead to:**

**Inconsistencies: Smart contracts using the precompiled contract may behave differently on different clients.**

**Security Risks: Variances could introduce vulnerabilities or unexpected behaviors.**

**Compatibility Issues: Transactions or contracts that work on one client might fail on another.**


### 3]  Using Remix write a simple contract that uses a memory variable, then using the debugger step through the function and inspect the memory.


```
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.0;

contract MemoryAndTransactionExample {
    function storeDataInMemory(uint256 x) public pure returns (uint256) {
        uint256 result;
        result = x * 2;
        return result;
    }

    receive() external payable {
        // This function is called when Ether is sent to the contract.
        // It doesn't perform any operation other than receiving Ether.
    }
}

```

**// Remix may not provide a transaction hash because pure functions do not create transactions on the Ethereum blockchain. so used receive() external payable to get transaction hash**



![Screenshot 2023-10-14 at 7 27 20 PM](https://github.com/Disha1998/ECode-AdvanceSolidity-2023/assets/69969675/215473af-831d-4f54-8a9b-d650fca1b43c)
