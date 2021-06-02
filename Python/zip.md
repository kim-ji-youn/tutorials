* **문제**: 이차원 리스트를 인자로 받아 원소의 행과 열을 뒤집은 값을 리턴      
ex) 
mylist = \[\[1, 2, 3\], \[4, 5, 6\], \[7, 8, 9\]\]
return value = \[\[1, 4, 7\], \[2, 5, 8\], \[3, 6, 9\]\]

내가 푼 방식
```
def solution(mylist):
    answer = []
    for i in range(len(mylist)) :
        line = []
        for j in range(len(mylist[i])) :
            line.append(mylist[j][i])
        answer.append(line)
    return answer
```

파이썬스러운 방식
```
def solution(mylist) :
    return list(map(list, zip(*mylist)))
```

**zip**함수
zip(): Returns an iterator of tuples, where the i-th tuple contains the i-th element from each of the argument sequences or iterables.

* 사용 예시 1
```
>>>list1 = [1, 2, 3]
>>>list2 = [10, 20 , 30]
>>>for i in zip(list1, list2) :
        print(i)
(1, 10)
(2, 20)
(3, 30)
```

* 사용 예시 2 - 여러 개의 iterable 동시에 순회해야할 때
```
>>>list1 = [1,2,3,4]
>>>list2 = [10, 20, 30, 40]
>>>list3 = [100, 200, 300, 400]
>>>answer = []
>>> for num1, num2, num3 in zip(list1, list2, list3) :
        print(num1+num2+num3)
111
222
333
444
>>>for i in zip(list1, list2, list3) :
        print(i)
(1, 10, 100)
(2, 20, 200)
(3, 30, 300)
(4, 40, 400)
```

* 사용 예시 3 - key와 value 리스트로 딕셔너리 만들기

```
>>>animal = ['cat', 'dog', 'lion']
>>>sounds = ['meow', 'woof', 'roar']
>>>answer = dict(zip(animals, sounds))
>>>print(answer)
{'cat':'meow', 'dog':'woof', 'lion':'roar'}
```




```
