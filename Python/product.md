'ABCD'와 'xy'의 곱집합은 'Ax, Ay, Bx, By, Cx, Cy, Dx, Dy'이다. 
곱집합을 구하기 위해서 보통 이런 코드를 사용했었다..

```
iterable1 = 'ABCD'
iterable2 = 'xy'

for v1 in iterable1 :
  for v2 in iterable2 :
    print(v1,v2)
```

하지만 ```itertools.product```를 통해 for문을 사용하지 않고 곱집합을 구할 수 있다. 

```
import itertools

iterable1 = 'ABCD'
iterable2 = 'xy'
print(list(itertools.product(iterable2, iterable2)))
```
