<div align="center">
  
# Query
</div>
</br>

# 1. Elementwise comparisons

| symbol | meaning |
|------|------|
| == | equal to |
| != | not equal to |
| < | less than |
| <= | less than or equal to |
| > | greater than |
| >= | greater than or equal to |

# 2. Multiple conditions
## And: `&`
## Or: `|`
## Negation: `~`
## Xor: `^`
## E.g. 
```Python
salaries[(salaries.get('POSITION') == "PG") | (salaries.get('POSITION') == "SG")]
```
# 3. Groupby
## Basic command: ` .groupby(column_name) `
* ### to gather rows which have the same value in the specified column
* ### Apply an aggregation function within each group
* ### The aggregation is applied individually to each column
* ### Change index label to "column_name"
## Aggregation functions: `.count() , .sum() , .mean() , .median() , .max() , .min(), .size() `
* ### Put numeric_only=True in "()"
## To rename a column:
* ### Add a new column with `.assign` containing the same values as the old column(s)
* ### Drop the old column(s) with `.drop(columns=list_of_column_labels)`
## `.str.len()` can give the string length of a title

