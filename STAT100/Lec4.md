<div align="center">
  
# Array

<br>
</div>

# 1. List
* ## Declaration: `varib=[num1,num2...]`
* ## Average of a *List*: `sum(List)/len(List)*
# 2. Array
* ## *Pre declaration:* `Import numpy as np`  
* ## arrays make it easy to perform the same operation to every element
* ## Declaration:`Array=np.Array([num1,num2,...])`
## 2.1 Array Number Arithmetic
* ### Increase/Decrease all numbers: `Array=Array + - num`
* ### Multiply/Divide all numbers: `Array=Array * / num`
## 2.2 Array Array Arithmetic
* ### *Array_1* and *Array_2* are previously declared
* ### `Array_1 + Array_2`
* ### `Array_1 - Array_2`
* ### `Array_1 * Array_2` 
* ### This command allows Array_1[m]*Array_2[m] to multiply and output
## 2.3 Basic Array Commands
* ### Length of Array: `len(Array)`
* ### Sum of Array: `sum(Array)` or `Array.sum()
* ### Average of Array: `sum(Array)/len(Array)` or Array.mean
* ### Maximum number in Array: `max(Array)` or `Array.max()`
## 3. Range
* ### An array of increasing integers from 0 up to (and excluding!) end: `np.arange(end)`
* ### An array of increasing integers from start up to (excluding!) end: `np.arange(start, end)`
* ### A range with step between consecutive values: `np.arange(start, end, step)`
* ### Examples:
```Python
np.arange(8) -> array([0, 1, 2, 3, 4, 5, 6, 7]) //Python
np.arange(3, 9, 1) -> array([3, 4, 5, 6, 7, 8]) //Python
np.arange(1, -10, -3) -> array([ 1, -2, -5, -8]) // Python
```
*******
*******
<div align="center">
  
# Panda

<br>
</div>

## 1. Definition
* ## *Panda* is a library of data processing tools.
* ### Predeclaration:`Import panda as pd` `Table = pd.read_csv('file.csv').take(np.arange(n))`
  * ###    It generates n lines from file.csv
## 2. Basic functions
* ### Setting the head index for file.csv: `Table.set_index(column_name)`
* ### Listing all the titles in file.csv: `Table.index`
    * ### Listing specific title in file.csv: `Table.index[number]`
* ### Shape of a table: `Table.shape()` Access each with `[title]`
    * ### Column: `Table.shape[0]`
    * ### Row: `Table.shape[1]`
* ### Get a column: `Table.get['title']`
* ### Assignment command: `Table=Table1.assign(Assignment clauses)` This command can create a new column/row in "Table"
* ### Get a row: `Table.loc['title']`
  * ### Get a specific row: `Table.iloc[number]`
* ### Sort the table in ascending order: `Table.sort_values(by='tilte')`
  * ### Descending: `Table.sort_values(by='tilte', ascending=False)`
* ### Booling Indexing: `Table[Table.get('title')>,<,==number]`
