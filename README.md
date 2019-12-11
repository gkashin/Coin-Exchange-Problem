# Coin-Exchange problem
The algorithm solves the well-known coin exchange problem. As a result, we get the number of coins needed to exchange a certain amount,
as well as the denomination of each coin

## Complexity
The complexity of such algorithm depends on exchange amount **V** and number of different coins **N** and equals **O(V*N)**

## Input Data
The input of the Horn-formula is divided into parts which look like this:
* *varCount* - number of variables
* *variables* - variables written with a space
* *implicationClausesCount* - number of implication clauses
* *implicationClauses* - list of the implication clauses represented as follows: x y z > w (**>** - means implication)
* *pureNegativeClausesCount* - number of pure negative clauses
* *pureNegativeClauses* - list of the pure negative clauses represented as follows: x y z; (separated by semicolon)

## Example
### Input
1. (w ∧ y ∧ z → x) ∧ (x ∧ z → w) ∧ (x → y) ∧ (→ x) ∧ (x ∧ y → w) ∧ (¬z)
```
4 // number of variables
x y z w // variables
5 // number of implication clauses
w y z > x // implication clauses
x z > w
x > y
> x
x y > w
1 // number of pure negative clauses
z; // pure negative clause
```
2. (w ∧ y ∧ z → x) ∧ (x ∧ z → w) ∧ (x → y) ∧ (→ x) ∧ (x ∧ y → w) ∧ (¬w ∨ ¬x ∨ ¬y) ∧ (¬z)
```
4 
x y z w 
5 
w y z > x 
x z > w
x > y
> x
x y > w
2 
w x y;
z; 
```
### Output
1. Satisfying set of variable values
```
w: 1
x: 1
y: 1
z: 0
```
2. Message of unsatisfiability
```
Function is not satisfiable
```
