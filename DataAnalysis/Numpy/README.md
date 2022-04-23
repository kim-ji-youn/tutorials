## Numpy
* Numerical Python
    * 대규모 다차원 배열을 다룰 수 있게 도와주는 라이브러리
    * numpy는 list에 비해서 빠른 연산을 지원하고, 메모리를 효율적으로 사용
    * numpy 라이브러리는 효율적인 데이터분석이 가능하도록 N차원의 배열 객체를 지원

### 배열 만들기
* Python list와 다르게 array는 단일 타입으로 구성되어 있음
* 배열 데이터 타입 dtype
    * int : 정수형 타입(i, int_, int32, int64, i8)
    * float: 실수형 타입(f, float_, float32, float64, f8)
    * str: 문자열 타입(str, U, U32)
    * bool: 부울 타입(?, bool_)

### 다양한 데이터 만들기
* np.array - 배열생성
* np.zeros - 0이 들어있는 배열 생성
* np.ones - 1이 들어있는 배열 생성
* np.empty - 초기화가 없는 값으로 배열을 반환
* np.arange(n) - 배열 버전의 range 함수
* np.random - 다양한 난수가 들어있는 배열 생성
ex) 0이상 10 미만의 랜덤한 값이 들어있는 2\*4크기의 배열을 변수 array에 저장합니다.
```array = np.random.randint(0, 10, (2,4))```

### 배열의 기초
