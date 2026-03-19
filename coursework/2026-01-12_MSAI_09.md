
## What I Learned

1. File Path Handling in Python
2. pathlib Module (Best Practice)
3. Pandas Dictionary Methods
| Method | Use Case | Safe? |
|--------|----------|-------|
| `dict[key]` | Direct access | KeyError if missing |
| `dict.get(key)` | Safe access | Returns None if missing |
| `df['col'].map(dict)` | Column mapping | Returns NaN if missing |

4. iloc vs loc
- `iloc` = **i**nteger position (row number)
- `loc` = **l**abel (index value)
- Use `.iloc[0]` to extract single value from Series

5. Useful Pandas Methods
- `ffill()` - Forward fill NaN with previous value
- `drop('col', axis=1)` - Delete column
- `isnull().sum()` - Count NaN values
- `pd.concat([df1, df2], axis=0)` - Combine dataframes (list required)
