# 제주코딩베이스캠프 섹션 1 문제 3,4,5

## 1. 문제 설명

#### 문제 3. 다음 출력 값으로 올바른 것은?

	var arr=[100,200,300];

	console.log(typeof(arr));

	1) undefined 
	   
	2) string  
	   
	3) number 
	   
	4) object



#### 문제 4. 다음 변수 a를 typeof(a)로 넣었을 때 출력될 값과의 연결이 알맞지 않은 것은?

   	1) 입력:a=1,  출력:number 

   	2) 입력:a=2.22  출력:boolean 

   	3) 입력:a='p'  출력:string 

   	4)  입력:a=[1,2,3]  출력:object 



#### 문제 5. 다음 코드의 출력 값으로 알맞은 것은?

	var a=10; 

	var b=2;

	for(var i=1; i<5; i+=2){
		a+=i;
	}

	console.log(a+b);


   	1) 10

   	2) 12

  	3) 14

   	4) 16


## 2. 내 풀이

#### 문제 3. 
	4번 object이다.


#### 문제 4. 
	2번 입력:a=2.22  출력:boolean이다.


#### 문제 5. 
 	4번 16이다.


## 3. 강의 해설

#### 문제 3.
	원시 타입이 아니면 다 object 타입이므로 4번 object이다.
   
#### 문제 4.
	2번 입력:a=2.22  출력:boolean이다. boolean은 true, false 두 가지 값밖에 없다.

#### 문제 5.
	a는 14, b는 2이므로 합해서 16이다.



***

인용한 강의 : 제주코딩베이스캠프 Code Festival: 자바스크립트 100제
