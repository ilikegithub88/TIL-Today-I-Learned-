# 리액트 에러 : [HMR] Waiting for update signal from WDS...

1. 문제점
   
    컴포넌트를 반복시키는 작업을 하는데 [HMR] Waiting for update signal from WDS... 메시지가 콘솔에 출력되면서 원하는 결과가 나오지 않았다.

2. [HMR] Waiting for update signal from WDS...에 초점 맞춰서 해결하려고 시도한 방법들
 
   2-1. 
    package.json 파일에서 version을 0.1.0 에서 3.2.0으로 수정하였다. 그리고 node_modules 폴더를 삭제하고 npm install했다.
    
   2-2. 
    https://webpack.js.org/guides/hot-module-replacement/#enabling-hmr 를 참조하고 webpack.config.js 파일을 찾았지만 못 찾았다.
   
    2-3. 
    webpack.config.js 파일을 직접 세팅해야하나 생각하다가 어제 겪은 에러처럼 코드 자체 문제일 수도 있다는 생각이 들었다.

3. 코드 자체에 초점 맞춘 해결책
   
   처음에 못 찾았던 오타를 찾아 수정하니 간단하게 해결되었다.
