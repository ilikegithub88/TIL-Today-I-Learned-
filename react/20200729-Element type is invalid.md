## 리액트 에러 : Error: Element type is invalid: expected a string (for built-in components) or a class/function (for composite components) but got: object.

### 1. 문제점
 
npm start 시켰더니 'Error: Element type is invalid: expected a string (for built-in components) 

or a class/function (for composite components) but got: object.' 메세지가 뜨면서 

에러의 원인으로 index.js, webpack의 어느 파일 등 여러 파일의 코드를 지목하는 페이지가 떴다.

너무 긴 에러 메세지가 나와서 당황했다.

### 2. 시도한 방법들
   
2-1. 에러 페이지가 index.js를 언급해서 다른 리액트 index.js와 코드 비교했다.

2-2. stackoverflow 들어갔더니 이 에러의 원인이 한 가지가 아니라 여러 가지라고 언급하는 글이 있었다. 

그래서 에러 메시지가 지목한 원인보다는 다른 코드가 문제일 수 있다는 생각이 들었다.


### 3. 해결책
   
연습용으로 만든 컴포넌트에서 메서드가 오류나길래 그 코드를 다 지워버렸지만 App.js에서 그 파일을 import하고 컴포넌트 관련 코드가 있는 상태였다.

App.js에서 그 컴포넌트 관련 코드를 지워버리니 에러 메시지가 사라졌다.
