# concurrently

 ## 정의
 npm 모듈이고 노드랑 리액트를 각자 따로 킬 필요없이 한꺼번에 부팅하게 한다.

## 활용 방법

   1. 터미널에 npm install concurrently 입력하고 설치한다.
         
   2. package.json 파일에서 scripts 항목에 "dev":"concurrently \"노드 서버 실행 명령\" \"리액트 실행 명령\""라고 입력한다.
        
      예를 들어 노드 부팅할 때 npm run start 라고 입력하면 앞부분은 "dev":"concurrently \"npm start\"라고 입력하고

      리액트 부팅할 때 client 폴더 경로 들어가서 npm run start 라고 입력하면 뒷부분은 \"npm start --prefix client\"" 라고 입력한다.

      합쳐서 package.json에 작성한 코드는 "dev":"concurrently \"npm start\" \"npm start --prefix client\"" 이다.

   3. 터미널에 npm run dev 라고 입력하면 노드와 리액트가 동시에 부팅된다.

