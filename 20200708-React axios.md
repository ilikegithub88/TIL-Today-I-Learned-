# 리액트 axios

+ javascript-exercise 저장소에 올린 weather_api 앱을 만들 때 fetch를 사용한 적 있지만 리액트의 axios는 사용한 적이 없었다.
+ axios를 사용하려면 먼저 터미널에 npm i axios 명령어를 입력해서 모듈을 설치해야 한다.
+ App.js 파일 상단에 import axios from "axios"; 라고 명시한다.
+ axios 실행 속도가 느려 비동기적 실행이 되므로 아래처럼 async await를 사용한다.
  
    > getMovies=async ()=>{
    >
    >       const {data: {data: {movies}}} = 
    >
    >       await axios.get("가져올 json");
    >
    > }