# Project Title

Implementation if require(),assert() and revert().

## Description
In this Solidity assessment we have created a smart contract in which we have created a contract with name assessment and inside that contract first we have declared a public variable with name val that is global.
After that we have declared a function with name set and in which we are passing new value and this is public,now we have used require that will check the condition if the condtion is satisfied then only the process will execute else it will be reverted back.After that we have used the assert that will check internal conditions after the exectution of the program.In this assert we are _new + val should be greater than val if this condtion is satisfied than the new value will be assigned to val that is old value.In the last we have created a revert funtion that will just revert an error if some errors have been encountered.

## Getting Started

### Installing

this code we are running on the online Solidity IDE that is https://remix.ethereum.org/ 
here we'll perform the code. as we are on the remix website just by clicking on th start coding we'll able to do coding in Solidity.

### Executing program
```
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.0;

contract Assessment {
    uint256 public val;

    function set(uint256 _new) external {
        // Use require() to validate conditions and revert if they are not met
        require(_new > 0, "Value must be greater than 0");

        // Use assert() for internal consistency checks (e.g., overflow)
        assert(_new + val >= val);

        // Set the new value
        val = _new;
    }

    function Revert() external pure {
        // Explicitly trigger a revert
        revert("This transaction intentionally reverted");
    }
}

```



## Authors

Contributors names and contact info

name-Sehaj deep singh.
email-sahejdeeps7@gmail.com


## License

This project is licensed under the sehaj deep License - see the LICENSE.md file for details
