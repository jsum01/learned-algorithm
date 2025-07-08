# learned-algorithm

**ps-language**: java

## 큰 수(BigInteger)
- package: java.math
- 범위: Integer.MAX_INTEGER( +- 10의 6억승)
### 선언
```java
BigInteger num = new BigInteger("10000"); // 초기 인자: String
```
초기 인지가 String이라는 것은 내부 동작이 문자열을 통해 이루어진다는 것을 의미.
### 상수
`ZERO`, `ONE`, `TWO`, `TEN`이라는 상수 키워드를 사용하여 가시적인 연산이 가능하다.
- 예시
    ```java
    BigInteger.TWO.pow(i).subtract(BigInteger.ONE); // 2^i - 1
    BigInteger.TWO.multiply(BigInteger.TWO); // 2 x 2
    ```
### 연산
- A + B = A.add(B)
- A - B = A.subtract(B)
- A * B = A.multiply(B)
- A / B = A.divide(B)
- A % B = A.remainder(B)
- A^B(제곱) = A.pow(B)
- A 제곱근 B = A.sqrt(B)
### 비교
Math 클래스 안에 있으며 String으로 내부 동작이 진행되기 때문에 BigInteger 자료형은 Math와 String에 있는 메서드와 유사한 메서드를 제공한다.
- A.equals(B): 두 값이 같은지 비교
- A.compareTo(B): 
    - A > B: 1
    - A = B: 0
    - A < B: -1
- A.max(B): 두 값 중 큰 값 반환
- A.min(B): 두 값 중 작은 값 반환
- A.bitCount(): A를 이진수로 변환했을 때 1의 개수 반환
### 형변환
- BigInteger to another(`.자료형+Value`)
```java
  BigInteger num = new BigInteger("10000");	// 선언

  int int_num = num.intValue();		// int
  long long_num = num.longValue();	// long
  float f_num = num.floatValue();		// float
  double d_num = num.doubleValue();	// double
  String s10_num = num.toString();		// 10진수 String <- 이것만 다름!!
  String s2_num = num.toString(2);   // 2진수 String -> 괄호 안에 2,8,16 가능
```
- `Exact` 형변환
  메서드 이름 끝에 `Exact`를 붙일 경우 형변환 결과가 해당 타입의 범위에 속하지 않으면 Exception을 발생시킴. (ex. `intValueExact()`)
- another to BigInteger(`.BingInteger.valueOf()`)
  ```java
  BigInteger num = BigInteger.valueOf(1000);
  ```
