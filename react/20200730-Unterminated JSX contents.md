## 리액트 에러 : Parsing error: Unterminated JSX contents

### 1. 문제점

윈도우 10, 크롬 84.0.4147.105(공식 빌드) 버전을 사용 중이고 npx create-react-app으로 만든 리액트에서

Parsing error: Unterminated JSX contents 메시지가 떴다.




### 2. 시도한 방법들

2-1. 에러가 난 위치가 </> 근처라서 그 근처를 살펴보았다.

            Line 20:12:  Parsing error: Unterminated JSX contents

                <button onClick={onButter}>butter</button>

                <button onClick={onDelete}>delete</button>

            </>
            
                ^


2-2. 구글링하니 태그가 잘 안 닫혀서 생길 수 있는 에러라고 나왔다.

### 3. 해결책

에러 메시지가 지목한 곳과 먼 자리에 있는 <h1> 태그가 닫히지 않았었다. 닫아주니 해결되었다.

            <h1> {bread} <h1>  // </h1>으로 수정했다.

            <button onClick={onJam}>jam </button>
            