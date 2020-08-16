# 제주코딩베이스캠프 섹션 1 문제 19

## 1. 문제 설명

#### 문제 19. 공백으로 구분하여 두 숫자 a와 b가 주어지면, a의 b승을 구하는 프로그램을 작성하세요.


## 2. 내 풀이

#### 문제 19.
        const n = prompt('a와 b를 입력하세요.').split(' ');

        console.log(Math.pow(parseInt(n[0], 10), parseInt(n[1], 10)));

## 3. 강의 해설

#### 문제 19.
        const n = prompt('수를 입력하세요.').split(' ');

        console.log(Math.pow(parseInt(n[0], 10), parseInt(n[1], 10)));

***

인용한 강의 : 제주코딩베이스캠프 Code Festival: 자바스크립트 100제
