---
title: "Amazing JavaScript
date: "2024-09-14"
thumbnail: "/assets/img/thumbnail/js.jpeg"
---

# Amazing JavaScript
---

**인프런-Amazing JavaScript**


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

