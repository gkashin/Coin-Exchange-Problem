# Coin-Exchange Problem (Dynamic Programming)
The algorithm solves the well-known coin exchange problem. As a result, we get the minimum number of coins needed to exchange a certain amount,
as well as the number and denomination of each coin

## Complexity
The complexity of such algorithm depends on exchange amount **V** and number of different coins **N** and equals **O(V*N)**

## Input Data
* *volume* - total amount
* *count* - number of coins
* *coins[i]* - denomination of coin **i**

## Example
### Input
Let us have 3 coins in denominations of 1, 10 and 25. And we want to exchange sum of 30
```
30 // total amount
3 // number of coins
// denominations
1
10
25
```
### Output
```
30 = 0*(1) + 3*(10) + 0*(25), 3 coins
```
