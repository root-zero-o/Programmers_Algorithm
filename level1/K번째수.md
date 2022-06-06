# K번째 수
## 1. 문제
- 배열 ```array```의 i번째 숫자부터 j번째 숫자까지 자르고 정렬했을 때, k번째에 있는 수 구하기
- 배열 ```array```, ```[i, j, k]```를 원소로 가진 2차원 배열 ```commands```가 매개변수로 주어질 때, ```commands```의 모든 원소에 대해 앞서 설명한 연산을 적용했을 때 나온 결과를 배열에 담아 return 하도록 solution 함수 작성
- (제한사항)
    - ```array```의 길이는 1 이상 100 이하
    - ```array```의 각 원소는 1 이상 100 이하
    - ```commands```의 길이는 1 이상 50 이하
    - ```commands```의 각 원소는 길이가 3 이하

```javascript
function solution(array, commands) {
    var answer = [];
    return answer;
}
```


## 2. 나의 풀이
```javascript
function solution(array, commands) {
    let answer = [];
    
    for(let i = 0; i < commands.length; i++){
        answer[i] = array
                    .slice(commands[i][0]-1, commands[i][1])
                    .sort((a,b) => a-b)[commands[i][2]-1]
    }
    
    return answer;
}
```
- ```slice()```를 이용해 배열을 자르고, ```sort```를 이용해 정렬한 뒤 정해진 순서의 값을 꺼냄
- ```sort```는 compareFunction이 제공되지 않으면 유니코드 포인터 순서로 문자열을 비교해서 정렬함
- 따라서 숫자비교를 위해 ```sort((a,b) => a - b)```라는 함수를 넣어주었음!

## 참고
- [프로그래머스 문제](https://programmers.co.kr/learn/courses/30/lessons/42748)
