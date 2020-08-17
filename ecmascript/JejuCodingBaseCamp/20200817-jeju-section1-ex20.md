# 제주코딩베이스캠프 섹션 1 문제 20

## 1. 문제 설명

#### 문제 20. 공백으로 구분하여 두 숫자가 주어집니다. 두번째 숫자로 첫번째 숫자를 나누었을 때 그 몫과 나머지를 공백으로 구분하여 출력하세요.
        입출력

        입력 : 10 2
        
        출력 : 5 0

## 2. 내 풀이

#### 문제 20.
        let x=prompt('두 숫자를 입력하세요').split(' ');

        let xa=x[0]/x[1];

        let xb=x[0]%x[1];

        console.log(xa+' '+xb);

## 3. 강의 해설

#### 문제 20.
        const n = prompt('수를 입력하세요.').split(' ');

        const result = Math.floor(parseInt(n[0], 10) / parseInt(n[1], 10));

        const left = parseInt(n[0], 10) % parseInt(n[1], 10);

        console.log(result, left);

***

인용한 강의 : 제주코딩베이스캠프 Code Festival: 자바스크립트 100제
