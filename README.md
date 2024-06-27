### [Writing An Interpreter In Go](https://interpreterbook.com/)

**Monkey Language** 

C계열 언어 기반으로 만든 저자의 학습용 동적 프로그래밍 언어이다.

Monkey 언어에서는 String, Integer, Boolean 타입을 지원하며 Character 타입은 없다.</br>
Monkey 언어에서 함수는 일급 함수이며 Closure를 지원한다.<br/>
Monkey 언어에서는 Javascript와 유사한 Array와 Object 타입을 지원한다.<br/>
Monkey 언어에서는 매크로를 지원한다.

아래는 Monkey 언어로 작성한 코드이다.

```monkey
// Array
let myArray = [1, 2, 3];
myArray[2]; // 3

// Object
let a = {"hello": "world"};
a["hello"]; // "world"

// Function
let plus = fn(x, y){ return x + y };
plus(1, 1); // 2

// Closure
let plus  = fn(x){ return fn(y){ return x + y }};
plus(1)(1); // 2

// Macro
let quotedInfixExpression = quote(4 + 4);
quote(unquote(4 + 4) + unquote(quotedInfixExpression))
```
