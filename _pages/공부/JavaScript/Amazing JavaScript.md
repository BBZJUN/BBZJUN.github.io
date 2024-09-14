---
title: "Amazing JavaScript
date: "2024-09-14"
thumbnail: "/assets/img/thumbnail/js.jpeg"
---

# Amazing JavaScript
---

**인프런-Amazing JavaScript**

강의영상 : https://www.inflearn.com/course/amazing-javascript-%EC%9E%85%EB%AC%B8

강의자료 : https://joshua1988.github.io/vue-camp/

온라인 IDE(코드샌드박스) : https://codesandbox.io/

### 개념

함수를 선언할 떄 쓰는 값: 파라미터(매개변수)
함수를 호출할 때 쓰는 값: 아규먼트(인자)


### 화살표 함수
```javascript

const foo = () => {
  console.log("foobar");
};
foo();

```


### 객체
자바스크립트는 객체 기반 언어입니다. 객체는 키(key) - 값(value) 형태로 이루어져 있으며 아래와 같은 형태를 갖습니다.

```javascript
var josh = {
  // 속성: 값
  language: 'javascript',
  coding: function() {
    console.log('Hello World');
  }
};
 
```

### 배열 API
1. push() : 배열에 데이터 추가 (맨 끝 인덱스부터 추가됨)
2. slice() : 배열의 특정 인덱스에 있는 값을 반환 (배열의 내용이 변환되지 않음)
3. splice() : 배열의 특정 인덱스에 있는 값을 변경 또는 삭제 (배열의 내용이 변경됨)
4. pop() : 배열의 마지막 인덱스의 값을 꺼냄 (배열의 내용이 변경됨)
5. shift() : 배열의 첫번째 인덱스의 값을 꺼냄 (배열의 내용이 변경됨)

```javascript
const array1 = ['a', 'b', 'c'];

array1.forEach((element) => console.log(element));
```

### Map

Map 객체는 키 와 값을 한 쌍으로 이루어진 컬렉션입니다.

```javascript
// map 선언
const map = new Map();

// map 값 추가 #1
map.set('key1', 'value1');
map.set('key2', 'value2');

// map 값 추가 #2
map
  .set('key1', 'value1')
  .set('key2', 'value2');

console.log(map); // Map(2) { 'key' => 'value', 'key2' => 'value' }

// map 값 삭제
map.delete('key1')
console.log(map); // Map(1) { 'key2' => 'value2' }

// map 모든 값 삭제
map.clear();
console.log(map); //Map(0) {}

map.forEach((val, key) => {
  console.log(val + "," + key);
});

// value 값 가져오기
for (const value of map.values()) {
    console.log("value : " + value);
}

// entries 반복문
for (let[key, value] of map.entries()) {
    console.log(key + " : " +value);
}

```


### Set

```javascript
// set 선언
const set = new Set();

// set 값 추가 #1
set.add('javascript');
set.add('vue');
set.add('node');

// set 값 추가 #2
set.add('javascript').add('vue').add('node');

console.log(set); // Set(3) { 'javascript', 'vue', 'node' }

// set 값 삭제
set.delete('banana')
console.log(set); // Set(2) { 'apple', 'orange' }

// set 전체 값 삭제
set.clear();
console.log(set); // Set(0) {}

// set 값 순회
set.forEach((val, val2, set) => {
 console.log(val, val2, set);
});

for (const val of set) {
 console.log(val);
}

// key 값 가져오기
for (const key of set.keys()) {
   console.log(key);
}

// value 값 가져오기 , set 에서 values() 는 keys()와 같습니다.
for (const value of set.values()) {
   console.log(value);
}

// 추가된 순서대로 반환됩니다.
for (const [key, value] of set.entries()) {
   console.log("key" + " = " + key);
   console.log("value" + " = " + value);
}

```

### forEach안에 함수

```javascript

var arr = [10,20,30];
var newArr = [];

arr.forEach(fuction(item) {
    newArr.push(item);
});

```


### filter

원하는 특정요소들을 꺼내옴

배열이름.filter


### 템플릿 리터럴

```javascript

` -> 이름은 백틱
이 백틱(`)을 사용해서
`${변수명}` 이렇게 쓸 수 있다

```

### 디스트럭쳐링(구조 분해 문법)

```javascript

var arr = ['apple',10]

var [fruit, num] = arr;
// 로 하면 fruit에 'apple', num에 10이 들어간다

//////
var josh = {
  language: 'javascript',
  position: 'front-end',
  area: 'pangyo',
  hobby: 'singing',
  age: '102'
};

var { language:별칭, position, area, hobby, age } = josh;
// :별칭 이름을 써서 이름을 바꿀 수 있다
console.log(language); // javascript
console.log(position); // front-end
console.log(area); // pangyo
console.log(hobby); // singing
console.log(age); // 102
 

```


### 스프레드 오퍼레이터 

... 으로 분리해서 넣는다

```javascript
// obj 객체를 newObj 객체에 복제
var obj = {
  a: 10,
  b: 20
};
var newObj = {...obj};
console.log(newOjb); // {a: 10, b: 20}

// arr 배열을 newArr 배열에 복제
var arr = [1,2,3];
var newArr = [...arr];
//var newArr = [...arr, 30, 50];
//이렇게 추가도 할 수 있다.
console.log(newArr); // [1, 2, 3]
 

```


### 모듈화

#### Import & Export

```javascript
// math.js
export var pi = 3.14;
export function sum(a, b) {
  return a + b;
}
 
 
// app.js
import { pi } from './math.js';
import { sum } from './math.js';
// import { pi, sum } from './math.js';
//한번에 불러와도 된다
console.log(pi); // 3.14
```

#### default
파일에서 하나를 꺼내겠다.
{} 이 괄호가 없다.

```javascript
// math.js
export default var pi = 3.14;
 
 
// app.js
import pi from './math.js';

console.log(pi); // 3.14

```


### 라이브러리

개발자가 편하게 구현할 수 있도록 미리 만들어 놓은 기능

```javascript

import 라이브러리이름 from "라이브러리이름"
Lodash 라는 라이브러리 추천함

```


### 비동기처리
자바스크립트의 비동기 처리란 특정 코드의 연산이 끝날 때까지 코드의 실행을 멈추지 않고 다음 코드를 먼저 실행하는 자바스크립트의 특성을 의미합니다.

```javascript

function fetchMenu(callbackFunction){
    setTimeout(() =>{
        //# 2
        let data = {firstMenu: "구독"};
        callbackFunction(data);
        return data;
    }, 5000);
}

let menu;
menu = fetchMenu(function (result) {// 익명함수
    // 호출되면 실행될 코드를 넣어주세여
    console.log("5초 뒤 실행", result);
});
//#1
console.log("출력 결과", menu);
//아직 값이 안나와서 여긴 언디파인드뜸
```


### Promise - 프로미스

프로미스는 자바스크립트 비동기 처리에 사용되는 객체입니다. 여기서 자바스크립트의 비동기 처리란 ‘특정 코드의 실행이 완료될 때까지 기다리지 않고 다음 코드를 먼저 수행하는 자바스크립트의 특성’을 의미합니다. 

https://joshua1988.github.io/web-development/javascript/promise-for-beginners/

```javascript

.then(); //성공
.catch(); //실패
```