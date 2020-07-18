# reactstrap
## 특징
 - css 프레임워크로서 인기를 얻던 부트스트랩을 리액트로 가져온 UI 라이브러리이다.
 - 부트스트랩을 이용한 다른 모듈도 있지만 reactstrap이 부트스트랩 4 버전을 지원한다.
 - 타입스크립트로 작성된 blueprint 라이브러리 등에 비해 reactstrap은 진입 장벽이 낮다.

## 사용 방법
    1. 터미널에 다음 명령어 입력해서 모듈 설치한다.
    > npm install --save reactstrap react react-dom

    2. 부트스트랩 설치한다.
    > npm install --save bootstrap

    3. 리액트스트랩 설치한다.
    > npm install --save reactstrap react react-dom

    4. index.js 파일에서 다음을 import한다.
    > import 'bootstrap/dist/css/bootstrap.min.css';

    5. 원하는 컴포넌트 삽입하기 위해 해당 소스를 홈페이지에서 복사한다. 여러 컴포넌트가 있지만 3가지만 추렸다.

        5-1. Card형 컴포넌트의 경우
            5-1-1. 미리 빈 리액트 파일을 준비한다.
            5-1-2. https://reactstrap.github.io/components/card/ 을 방문한다.
            5-1-3. 검은 화면 소스에서 import {Card, CardImg, CardText, CardBody, CardTitle, CardSubtitle, Button } from 'reactstrap';를 복사해서 리액트 파일에 붙여넣는다.
            5-1-4. 검은 화면 소스에서 return 안에 있는 <Card>로 시작하고 </Card>로 끝나는 소스를 복사해서 빈 리액트 파일에 붙여넣는다.
            5-1-5. 해당 리액트 파일을 편집하고 App.js 파일에서 그 리액트 파일을 import한다.
        5-2. 그리드 구역으로 나누는 경우
            5-2-1. 그리드 구역으로 구분하려는 리액트 파일에 import {Container,Row, Col} from 'reactstrap'; 넣는다.
            5-2-2. 그리드 구역으로 구분하려는 가장 바깥 영역의 className을 Container로 설정한다.
            5-2-3. 그 안에 <Row></Row>를 넣는다.
            5-2-4. <Row></Row> 안에 <Col></Col>을 넣는다.
            5-2-5. 사이즈를 조절하려면 `sm="3"` 이렇게 지정한다.
                (예시)
                <section className="Container">
                    <Row>
                        <Col sm="4">
                            popular plays
                        </Col>
                        <Col sm="7">
                            popular movies
                        </Col>            
                    </Row>
                </section>

        5-3. Navbar 컴포넌트의 경우

            5-3-1. 빈 리액트 파일을 준비한다.
            5-3-2. https://reactstrap.github.io/components/navbar/ 을 방문한다.
            5-3-3. 검은 화면의 소스를 전부 복사해서 리액트 파일에 붙여넣는다.

## 추천 튜토리얼
    유튜브에서 WalkThroughCode 유튜버의 영상을 추천한다.