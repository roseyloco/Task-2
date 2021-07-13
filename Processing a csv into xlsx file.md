```python
import pandas as pd
```


```python
df = pd.read_csv(r'C:\Users\Roselyne\Downloads\dummy.csv')
```


```python
df.set_index('Id', inplace=True)
```


```python
df[['first_name','last_name']]= df['Name'].str.split(' ',expand=True)
```


```python
df.dropna(how='all', axis=1, inplace=True)
```


```python
df
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Name</th>
      <th>first_name</th>
      <th>last_name</th>
    </tr>
    <tr>
      <th>Id</th>
      <th></th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>1</th>
      <td>Tobi Martins</td>
      <td>Tobi</td>
      <td>Martins</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Joseph Kiipo</td>
      <td>Joseph</td>
      <td>Kiipo</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Joseph Ita</td>
      <td>Joseph</td>
      <td>Ita</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Betty Blavo</td>
      <td>Betty</td>
      <td>Blavo</td>
    </tr>
    <tr>
      <th>5</th>
      <td>Samuel Osborne</td>
      <td>Samuel</td>
      <td>Osborne</td>
    </tr>
  </tbody>
</table>
</div>




```python
df.to_excel (r'C:\Users\Roselyne\Downloads\dummyOutput.xlsx')
```


```python

```
