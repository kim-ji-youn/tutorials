#### 4. Iterable 다루기
##### 4-3. 모든 멤버의 type 변환하기: map

* **문제**: \['1', '100', '33'\]을 \[1, 100, 33\]으로 변환하기

내가 짠 코드
```
def solution(mylist):
    answer = []
    for m in mylist :
        answer.append(int(m))
    return answer
```

map을 사용하면 for문을 사용하지 않고 멤버의 타입을 일괄적으로 변환할 수 있따. 
```
list1 = ['1', '100', '33']
list2 = list(map(int, list1))
```
