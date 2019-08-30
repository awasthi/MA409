

```python
def add(a,b):
    return a+b
```


```python
add(3,4)
```




    7




```python
P = " abcdefghijklmnopqrstuvwxyz"
C = " ABCDEFGHIJKLMNOPQRSTUVWXYZ"
KEY=3
#p - plaintext
def enc(p):
    c=""
    for x in p:
        pi=P.find(x)
        ci= (pi+KEY) % 27
        c = c + C[ci]
    return c

def dec(c):
    p=""
    for x in c:
        ci=C.find(x)
        pi= (ci-KEY) % 27
        p = p + P[pi]
    return p

```


```python
enc("hello")
```




    'KHOOR'




```python
enc("hello dear why are not meeting near sarovar")
```




    'KHOORCGHDUCZKACDUHCQRWCPHHWLQJCQHDUCVDURYDU'




```python
dec("KHOORCGHDUCZKACDUHCQRWCPHHWLQJCQHDUCVDURYDU")
```




    'hello dear why are not meeting near sarovar'




```python

```
