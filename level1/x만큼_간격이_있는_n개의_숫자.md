# x만큼 간격이 있는 n개의 숫자
## 1. 문제
- 정수 x와 자연수 n을 입력 받아, x부터 시작해 x씩 증가하는 숫자를 n개 지니는 리스트를 리턴하는 함수 ```solution``` 완성
- (제한조건) x는 -10000000 이상, 10000000 이하인 정수 / n은 1000 이하인 자연수

## 2. 나의 풀이
```javascript
function solution(x, n) {
    let answer = [];
       
    for(let i = 0; i < n; i ++){
        answer[i] = x * (i + 1)
    }    
    return answer;
}
```
- ```for```문을 이용해 나온 값을 ```answer```의 요소로 넣어 쉽게 풀 수 있었던 문제😎

## 3. 다른 풀이
```javascript
function solution(x, n) {
    return Array(n).fill(x).map((v, i) => (i + 1) * v)
}
```
```javascript
function solution(x, n) {
    return nNumbers(x,n);
}

const nNumbers = (x, n)=>{
    return Array.from({length: n},(v,index)=>(index+1)*x);
};

```
- array(), fill(), map(), 화살표함수 공부 후 정리해둘 것
