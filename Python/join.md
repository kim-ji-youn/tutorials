* **문제**: 리스트의 원소를 모두 이어붙인 문자열 리턴하기

파이썬스럽지 않은 코드
```
def solution(mylist):
    answer = ''
    for value in mylist :
        answer += value
    return answer
```

나는 join함수를 써서 파이썬스럽게 잘 짰다!
```
def solution(mylist) :
    return ''.join(mylist)
```

* **join()**함수
    * str.join(iterable)
