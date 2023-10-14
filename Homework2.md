
### Solidity
### 1. Write a function that will delete items (one at a time) from a dynamic array without leaving gaps in the array. You should assume that the items to be deleted are chosen at random, and try to do this in a gas efficient manner. For example imagine your array has 12 items and you need to delete the items at indexes 8, 2 and 7. The final array will then have items {0,1,3,4,5,6,9,10,11}
 

```
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.0;

contract DynamicArray {
    uint[] public dynamicArray; //created dynemic array

    function getArrayLength() public view returns (uint) {
        return dynamicArray.length; 
    }

    function getElement(uint index) public view returns (uint) {
        require(index < dynamicArray.length, "Index out of bounds");
        return dynamicArray[index];
    }

    function addElement(uint element) public {
        dynamicArray.push(element);
    }

    function deleteElement(uint index) public {
        require(index < dynamicArray.length, "Index out of bounds");

        if (index != dynamicArray.length - 1) {
            // Swap the element to delete with the last element in the array
            dynamicArray[index] = dynamicArray[dynamicArray.length - 1];
        }

        // Remove the last element to avoid leaving gaps in the array
        dynamicArray.pop();
    }

    function deleteRandomItems(uint[] memory indexes) public {
        require(indexes.length > 0, "No items to delete");

        for (uint i = 0; i < indexes.length; i++) {
            deleteElement(indexes[i]);
        }
    }
  
}

```




##### //you can delete element by mannually e.g: 0th index

##### //you can delete random elements by calling this 'deleteRandomItems' function where delete like [0,2,4] index elements will be removed from array
