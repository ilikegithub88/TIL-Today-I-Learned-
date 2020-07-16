# Destructuring (비구조화 할당, 구조 분해 할당)

## 1. 정의
비구조화 할당은 배열의 요소 중 하나를 콕 집어 사용할 수 있게 배열을 분해하는 것이다.

## 2. 예시 1
> const numbers=[1,2,3,4,5];
> 
> [number1, ,number3, ,number5] = numbers; 
> 
> console.log(number1, number3); 


[number1, ,number3, ,number5] = numbers; 에서 배열 numbers의 첫번째 요소 1은 number1에 할당되고 

콤마 뒤에 빈 칸이 있어서 numbers 배열의 요소 2는 건너뛴다.

numbers의 요소 3은 number3에 할당된다. 또 빈 칸이 있어서 numbers의 요소 4는 건너뛴다. 

5는 number5에 할당된다.
console.log(number1, number3); 때문에 1 3 이라고 콘솔에 출력된다.

## 3. 예시 2
> const city=['Seoul','Incheon','Busan','Guri'];
> 
> [,city2,city3,city4]=city;
> 
> console.log(city2,city3);

배열 city의 요소 'Seoul'은 건너뛰고 'Incheon'이 city2에 할당된다. 

'Busan'이 city3에 할당되고 'Guri'가 city4에 할당된다.


그래서 console.log(city2,city3) 때문에 콘솔에 Incheon Busan이라고 출력된다.

## 4. 사용 가능 브라우저
크롬, 사파리, 엣지, 파이어폭스, 오페라 브라우저에서 비구조화 할당을 지원한다.