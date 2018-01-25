# Water Walls

## Setup

### Strategy

Iterate through input, figure out tallest pairs of walls and amount of water in between them,
keeping track of the current walls with most water, return walls and amount of water

Input: [2, 4, 6, 2, 3, 9, 7, 5, 2, 10]
* each number represents the height of a wall
Output: [6, 10, 13]
* between wall #6 and wall #10, there are 13 blocks of water

### Big-O Notation
* O(n) since every wall is visited

### Transformation Steps
1. 2 -> 4 -> 6 increases
2. 6 -> 2 decreases so start at wall #3 (6) to find next wall taller or equal to 6
3. wall #6 (9) is next wall taller than 6
4. difference between wall #3 and #4 (6 - 2 = 4) + diff b/w wall #3 and #5 (6 - 3 = 3), sum is 7 (current max water)
5. start at wall #6 (9) and find next wall taller or equal to 9
6. wall #10 (10) is next wall taller than 9
7. diff b/w #6 and #7 (9 - 7 = 2) + diff b/w #6 and #8 (9 - 5 = 2) + diff b/w #6 and #9 (9 - 2 = 7), sum is 13 (now current max water)

### Function Skeleton
```
const waterWalls = () => {
  //constraints: none
  //initialize storage array
  //initiatize current max as 0
  //iterate through input array
      //find first index where following number is smaller
      //find index where next number is equal to or larger than number at first index, store both index in tuple in storage array
      //sum the differences of first index with each value in between the two stored indices, add to tuple in storage array and set as current max if larger than current max
      //second index becomes first index, repeat previous steps
  //return array containing current max
}
```

