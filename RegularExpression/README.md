# 정규 표현식(Regular Expression)
정규 표현식은 특정한 규칙을 가진 문자열의 집합을 표현하는 데 사용하는 형식 언어입니다.
여기서는 정규표현식의 문법을 정리해보겠습니다. 
[여기]에서는 정규식이 시각화된 것을 확인할 수 있습니다. 

[여기]: https://regexper.com/

#### 1. \[  \]
* \[와 \] 사이에 있는 요소들 중 하나라는 의미를 가집니다. 
* \[1234\]: 1 **or** 2 **or** 3 **or** 4
* \[1234abc\]: 1 **or** 2 **or** 3 **or** 4 **or** a **or** b **or** c

#### 2. ( | )
* (와 ) 사이에 |로 구분되는 요소들 중 하나라는 의미를 가집니다. 
* (1|2|3|4): 1 **or** 2 **or** 3 **or** 4
* (1|2|3|4|a|b|c) : 1 **or** 2 **or** 3 **or** 4 **or** a **or** b **or** c

#### 3. -
* 연속된 숫자 또는 알파벳을 표현할 수 있습니다. 
* \[1-4\] = \[1234\] = 1 **or** 2 **or** 3 **or** 4
* \[1-4a-c\] = \[1234abc\] =  1 **or** 2 **or** 3 **or** 4 **or** a **or** b **or** c

#### 4. \[^\]
* ^는 not의 의미를 가집니다. 
* \[^1-4\] = 1,2,3,4를 제외한 글자
* \[^1-4a-c\] = 1,2,3,4,a,b,c를 제외한 한 글자

#### 5. ( ) 
* 그룹
* (x)(yz)

#### 6. | 
* or('또는') 의미
* (x|y) = x **or** y

#### 7. ?
* 앞의 수식이 나타나지 않거나 한번만 나타남 (0 or 1)
* x? = {$$\0$$, x}

#### 8. +
* 앞의 수식이 한 번 이상 나타나는 경우
* x+ = {x, xx, xxx, xxxx, xxxxx, ...}

#### 9. *
* 앞의 수식이 나타나지 않거나 여러 번 나타나는 경우
* x+ = {$