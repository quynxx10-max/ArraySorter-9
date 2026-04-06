# ArraySorter-9
ArraySorter.sol
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.20;

contract ArraySorter {
    uint256[] public numbers;

    function addNumber(uint256 _num) public {
        numbers.push(_num);
    }

    function sort() public {
        for (uint i = 0; i < numbers.length; i++) {
            for (uint j = i + 1; j < numbers.length; j++) {
                if (numbers[i] > numbers[j]) {
                    (numbers[i], numbers[j]) = (numbers[j], numbers[i]);
                }
            }
        }
    }

    function getNumbers() public view returns (uint256[] memory) {
        return numbers;
    }
}
