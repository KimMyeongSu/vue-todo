## 변수,함수 스코프(function scope)와 블록 스코프(block scope) 
자바스크립트에는 다양한 변수 선언 키워드가 있다. 자바스크립트가 처음 등장할 때부터 사용되던 <code>var</code>와, 그리고 <code>var</code>의 부족함을 채우기위해 ES2015에서 새롭게 등장한 <code>let</code>과 <code>const</code>

<code>var</code> 변수는 아래와 같은 특징 있다.
<ol>
    <li>변수 이름 중복선언 가능</li>
    <li>변수 선언 전에 사용 가능(호이스팅)</li>
    <li>함수 스코프</li>
</ol>

특히나 중복된 이름으로 선언이 가능했던 특징은 여러 사람이 협업할 때 생각보다 자주 문제
이런 문제를 개선하기 위해 ES2015에서 let과 const가 등장
<code>let , const</code> 변수는 아래와 같은 특징 있다.
<ol>
    <li>변수 이름 중복선언 불가 (SyntaxError 발생)</li>
    <li>변수 선언 전에 사용 불가 (ReferenceError 발생)</li>
    <li>블록 스코프</li>
</ol>

var 키워드로 선언한 변수는 함수 스코프
let과 const 키워드로 선언한 변수는 블록 스코프
```javascript
function sayHi() {
  var userName = 'codeit';
  console.log(`Hi ${userName}!`);
}
//함수 안에서 선언한 변수는 함수 안에서만 유효
//var 선언시 for, if, while는 블록 밖에서도 유효
console.log(userName); // ReferenceError
```
```javascript
//let 과 const 는 블록 안에서만 유효
function sayHi() {
  const userName = 'codeit';
  console.log(`Hi ${userName}!`);
}

for (let i = 0; i < 5; i++) {
  console.log(i);
}

{
  let language = 'JavaScript';
}

console.log(userName); // ReferenceError
console.log(i); // ReferenceError
console.log(language); // ReferenceError
```


## 비동기 처리
### 1. callback
### 2. promise
### 3. promise + generater
### 4. async & await


