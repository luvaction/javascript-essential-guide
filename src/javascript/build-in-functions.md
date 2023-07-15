# Javascript Build-In Functions

## `index`

- [1. String](#string)
- [2. Array](#array)
- [3. Number](#number)
- [4. Math](#math)
- [5. global](#global)

## **string**

[go to Index](#index)

### `charAt()` 문자열에서 특정 위치의 문자를 반환

```javascript
let str = "Hello, World!";
console.log(str.charAt(0)); // 'H'
```

### `concat()` 두 문자열을 연결하여 새 문자열을 반환

```javascript
let str = "Hello, World!";
console.log(str.concat(" How are you?")); // 'Hello, World! How are you?'
```

### `indexOf()` 문자열에서 지정된 값이 처음으로 발생하는 인덱스를 반환

```javascript
let str = "Hello, World!";
console.log(str.indexOf("o")); // 4
```

### `lastIndexOf()` 문자열에서 지정된 값이 마지막으로 발생하는 인덱스를 반환

```javascript
let str = "Hello, World!";
console.log(str.lastIndexOf("o")); // 8
```

### `replace()` 문자열에서 일부 문자를 다른 문자로 교체

```javascript
let str = "Hello, World!";
console.log(str.replace("Hello", "Hi")); // 'Hi, World!'
```

### `slice()` 문자열의 일부를 추출하고 새 문자열을 반환

```javascript
let str = "Hello, World!";
console.log(str.slice(0, 5)); // 'Hello'
```

### `split()` 문자열을 배열로 분할

```javascript
let str = "Hello, World!";
console.log(str.split(",")); // ['Hello', ' World!']
```

### `substring(startIndex, endIndex)` 시작 인덱스부터 끝 인덱스 전까지의 문자열을 반환

인덱스는 0부터 시작하며, 시작 인덱스는 포함되고 끝 인덱스는 포함되지 않습니다. 또한, 시작 인덱스와 끝 인덱스의 순서에 관계 없이 항상 왼쪽에서 오른쪽으로 추출됩니다.

```javascript
let str = "Hello, World!";
console.log(str.substring(1, 4)); // 'ell'
```

### `substr(startIndex, length)` 시작 인덱스부터 지정된 길이만큼의 문자열을 반환

시작 인덱스는 0부터 시작 길이 인수는 추출할 문자열의 길이를 지정 예를 들어, `substr(1, 4)`는 인덱스 1부터 4개의 문자를 반환

```javascript
let str = "Hello, World!";
console.log(str.substr(1, 4)); // 'ello'
```

### `toLowerCase() toUpperCase()`

문자열을 소문자/대문자로 변환

```javascript
let str = "Hello, World!";
console.log(str.toLowerCase()); // 'hello, world!'
console.log(str.toUpperCase()); // 'HELLO, WORLD!'
```

### `trim()`

문자열의 양쪽 끝에서 공백을 제거

```javascript
let str = "Hello, World!";
console.log("    Hello, World!    ".trim()); // 'Hello, World!'
```

## **array**

[go to Index](#index)

### `concat()` 두 개 이상의 배열을 연결하고 결과를 새 배열로 반환

```javascript
let arr = [1, 2, 3, 4, 5];
console.log(arr.concat([6, 7, 8])); // [1, 2, 3, 4, 5, 6, 7, 8]
```

### `every()` 배열의 모든 요소가 테스트 함수를 통과하는지 확인

```javascript
let arr = [1, 2, 3, 4, 5];
console.log(arr.every((num) => num < 10)); // true
```

### `filter()` 테스트 함수를 통과하는 요소들로 새 배열을 생성

```javascript
let arr = [1, 2, 3, 4, 5];
console.log(arr.filter((num) => num % 2 == 0)); // [2, 4]
```

### `find()` 테스트 함수를 통과하는 첫 번째 요소를 반환

```javascript
let arr = [1, 2, 3, 4, 5];
console.log(arr.find((num) => num > 3)); // 4
```

### `forEach()` 배열의 각 요소에 대해 함수를 실행

```javascript
let arr = [1, 2, 3, 4, 5];
arr.forEach((num) => console.log(num)); // 1 2 3 4 5
```

### `join()` 배열의 모든 요소를 문자열로 결합

```javascript
let arr = [1, 2, 3, 4, 5];
console.log(arr.join("-")); // '1-2-3-4-5'
```

### `map()` 배열의 모든 요소에 대해 함수를 호출하고 결과를 새 배열로 반환

```javascript
let arr = [1, 2, 3, 4, 5];
console.log(arr.map((num) => num * 2)); // [2, 4, 6, 8, 10]
```

### `pop()` 배열에서 마지막 요소를 제거하고 반환

```javascript
let arr = [1, 2, 3, 4, 5];
console.log(arr.pop()); // 5
```

### `push()` 배열의 끝에 새 요소를 추가하고 새 길이를 반환

```javascript
let arr = [1, 2, 3, 4, 5];
console.log(arr.push(6)); // 6
```

### `shift()` 배열에서 첫 번째 요소를 제거하고 반환

```javascript
let arr = [1, 2, 3, 4, 5];
console.log(arr.shift()); // 1
```

### `unshift()` 배열의 시작 부분에 새 요소를 추가하고 새 길이를 반환

```javascript
let arr = [1, 2, 3, 4, 5];
console.log(arr.unshift(0)); // 5
```

### `slice()` 배열의 일부를 추출하여 새 배열을 생성

```javascript
let arr = [1, 2, 3, 4, 5];
console.log(arr.unshift(0)); // 5
```

- `slice()`: 배열의 일부를 추출하여 새 배열을 만듭니다.
- `splice()`: 배열에서 요소를 추가/삭제
- `reduce()`: 배열 요소의 각각에 대해 함수를 실행하고 단일 출력 값을 생성

## **number**

[go to Index](#index)

### `isFinite()` 값이 유한한 숫자인지 확인

```javascript
let num = 123.456;
console.log(isFinite(num)); // true
```

### `isNaN()` 값이 NaN인지 확인

```javascript
let num = 123.456;
console.log(isNaN(num)); // false
```

### `parseFloat()`: 문자열을 부동소수점 숫자로 변환

```javascript
let num = 123.456;
console.log(parseFloat("123.456")); // 123.456
```

### `parseInt()`: 문자열을 정수로 변환

```javascript
let num = 123.456;
console.log(parseInt("123.456")); // 123
```

### `toExponential()`: 숫자를 지수 표기법으로 변환

```javascript
let num = 123.456;
console.log(num.toExponential(2)); // '1.23e+2'
```

### `toFixed()`: 숫자를 고정 소수점 표기법으로 변환

```javascript
let num = 123.456;
console.log(num.toFixed(2)); // '123.46'
```

### `toString()`: 숫자를 문자열로 변환

```javascript
let num = 123.456;
console.log(num.toString()); // '123.456'
```

## **math**

[go to Index](#index)

### `abs()` 숫자의 절대값을 반환

```javascript
let num = 123.456;
console.log(Math.abs(num)); // 123.456
```

### `ceil()`: 숫자를 올림

```javascript
let num = 123.456;
console.log(Math.ceil(num)); // -123
```

### `floor()`: 숫자를 내립니다.

```javascript
let num = 123.456;
console.log(Math.floor(num)); // -124
```

### `max()`: 숫자의 최댓값을 반환

```javascript
let num = 123.456;
console.log(Math.max(1, 2, 3, 4, 5)); // 5
```

### `min()`: 숫자의 최솟값을 반환

```javascript
let num = 123.456;
console.log(Math.min(1, 2, 3, 4, 5)); // 1
```

### `random()`: 0 (포함)과 1 (미포함) 사이의 난수를 반환

```javascript
let num = 123.456;
console.log(Math.random()); // 0.xxxxxx
```

### `round()`: 숫자를 가장 가까운 정수로 반올림

```javascript
let num = 123.456;
console.log(Math.round(num)); // -123
```

### `sqrt()`: 숫자의 제곱근을 반환

```javascript
let num = 123.456;
console.log(Math.sqrt(9)); // 3
```

## **global**

[go to Index](#index)

### `decodeURI()` URI를 전체 URI로 디코드

```javascript
let uri = "https://www.example.com/?key=value";
console.log(decodeURI(uri)); // 'https://www.example.com/?key=value'
```

### `encodeURI()`: URI를 전체 URI로 인코드

```javascript
let uri = "https://www.example.com/?key=value";
console.log(encodeURI(uri)); // 'https://www.example.com/?key=value'
```

### `eval()`: JavaScript 문자열 식을 평가

```javascript
console.log(eval("2 + 2")); // 4
```

### `setTimeout()`: 일정 시간 후에 함수를 실행

```javascript
setTimeout(() => {
  console.log("Delayed message");
}, 1000);
```

### `setInterval()`: 일정 시간 간격으로 함수를 반복 실행

```javascript
setInterval(() => {
  console.log("Repeated message");
}, 2000);
```
