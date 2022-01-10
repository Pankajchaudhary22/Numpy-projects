```python
import numpy as np
```

# 1) Mean speed of all the cab rides


```python
cab=np.genfromtxt("nyc_taxis.csv",delimiter=",", skip_header=True)
```


```python
cab
```




    array([[2.016e+03, 1.000e+00, 1.000e+00, ..., 1.165e+01, 6.999e+01,
            1.000e+00],
           [2.016e+03, 1.000e+00, 1.000e+00, ..., 8.000e+00, 5.430e+01,
            1.000e+00],
           [2.016e+03, 1.000e+00, 1.000e+00, ..., 0.000e+00, 3.780e+01,
            2.000e+00],
           ...,
           [2.016e+03, 6.000e+00, 3.000e+01, ..., 5.000e+00, 6.334e+01,
            1.000e+00],
           [2.016e+03, 6.000e+00, 3.000e+01, ..., 8.950e+00, 4.475e+01,
            1.000e+00],
           [2.016e+03, 6.000e+00, 3.000e+01, ..., 0.000e+00, 5.484e+01,
            2.000e+00]])




```python
speed=cab[:,7]/(cab[:,8]/3600)
```


```python
Mean_speed=speed.mean()
```


```python
print(Mean_speed)
```

    32.24258580925573
    

# 2) Total numbers of rides taken in the february month


```python
rides=cab[cab[:,1]==2,1]

```


```python
rides.shape[0]
```




    13333



# 3)Number of rides where tip is greater than 50$


```python
Tip=cab[cab[:,-3]>50,-3]
```


```python
Tip.shape[0]
```




    16



# 3) Number of rides where drop location was JFK airport


```python
JFK=cab[cab[:,6]==2,6]
```


```python
JFK.shape[0]
```




    11832




```python

```
