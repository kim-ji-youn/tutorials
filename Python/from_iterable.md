#### 6. 
##### 6-2. 2차원 리스트를 1차원 리스트로 만들기

for문을 사용해서 이렇게나 비효율적으로 코드를 작성하였다. 
```
def solution(mylist):
    answer = []
    for i in range(len(mylist)) :
        for j in range(len(mylist[i])) :
            answer.append(mylist[i][j])
    return answer
```


아래와 같은 방법들은 효율적으로 2차원 리스트를 1차원으로 만들 수 있다. 
```
my_list = [[1, 2], [3, 4], [5, 6]]

#방법 1
answer = sum(mylist, [])

#방법 2
import itertools
list(itertools.chain.from_terable(my_list))

#방법 3
import itertools
list(itertools.chain(*my_list))

#방법 4
[element for array in my_list for element in array]

#방법 5
from functools import reduce
list(reduce(lambda x, y : x+y, my_list))

#방법 6
from functools import reduce
import operator
list(reduce(operator.add, my_list))


```
