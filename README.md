# Youtube API를 이용한 뷰티 사이트

## 작업 순서
1. node.js 설치 / 버전 확인 : node -v  / https://nodejs.org/ko 여기에서 다운
2. React.js 설치 : react npx create-react-app .
3. 폴더가 잘 만들어졌는지 확인하기 : npm start
4. 라이브러리 설치
5. 폴더 셋팅 : 필요없는 파일 제거
6. header 설정
7. Suspense 설정
8. 걱 페이지 메타 태그 설정(HelmetProvider)


## 인덱스   
1. 셋팅하기       
1_1. Node.js 설치    
1_2. Vscode 설치    
1_3. React.js 설치    
        
2. 라이브러리 설치하기    
2_1. 폴더 정리하기    
2_2. 라이브러리 설치하기    


### 실행하기
'npm start' : 리엑트 실행하기


### 1. 폴더 설명
- node_modules : 이 폴더는 프로젝트에서 사용하는 외부 라이브러리와 패키지들이 저장되는 곳입니다. 개발에 필요한 도구와 코드를 더 쉽게 관리할 수 있게 도와줍니다.
- ublic : 이 폴더는 프로젝트의 공용 파일들이 저장되는 곳입니다. 주로 HTML 파일과 이미지 같은 정적인 파일들이 이곳에 위치하며, 이 파일들은 웹 브라우저에서 직접 접근할 수 있습니다.
- favicon.svg : 웹 사이트의 아이콘을 나타내는 이미지 파일입니다. 웹 브라우저 탭에 표시되는 작은 아이콘을 설정할 수 있습니다.
- index.html : React 애플리케이션의 진입점인 HTML 파일입니다. 브라우저에서 앱을 로드할 때 사용됩니다.
- robots.txt : 이 파일은 웹 사이트의 검색 엔진 크롤러에게 어떤 페이지를 검색할 수 있고 어떤 페이지를 검색하지 말아야 하는지에 대한 지침을 제공하는 텍스트 파일입니다
- src : 이 폴더는 실제로 프로젝트의 소스 코드가 저장되는 곳입니다. 여기서 작성한 코드가 애플리케이션의 동작을 정의합니다.
- assets : 이미지나 폰트 등의 정적인 자원 파일들을 저장하는 폴더입니다.
- App.js : React 애플리케이션의 주요 컴포넌트인 App 컴포넌트의 코드가 들어있는 파일입니다. 이 파일에서 애플리케이션의 구조와 기능을 정의할 수 있습니다.
- index.js : React 애플리케이션의 진입점인 JavaScript 파일입니다. 이 파일에서 React 앱을 DOM에 렌더링하는 역할을 합니다.
- .gitignore : Git 버전 관리에서 제외할 파일이나 폴더를 설정하는 파일입니다. node_modules와 같이 불필요한 파일들을 Git에 올리지 않도록 할 때 유용합니다.
- package-lock.json : 패키지 의존성을 관리하기 위한 자동 생성된 파일입니다. 이 파일은 패키지들의 버전 및 의존 관계를 정확하게 유지하기 위해 사용됩니다.
- package.json : 프로젝트 설정과 의존성 정보를 담고 있는 파일입니다. 프로젝트의 이름, 버전, 필요한 라이브러리 등을 정의할 수 있습니다.
- README.md : 프로젝트에 대한 설명과 사용 방법을 기술하는 마크다운 파일입니다. 다른 개발자들이 프로젝트를 이해하고 사용하는데 도움이 되는 정보를 작성할 수 있습니다.


### 2. 필요한 라이브러리 설치
- react를 설치 `npm create-react-app 폴더이름` : 폴더를 생략하고 싶으면 .으로 표시
- react-router-dom 설치 `npm install react-router-dom` : 주소를 설정하기 위한 라이브러리
- axios 설치 `npm install axios` : API 라이브러리
- react icon 설치 `npm install react-icons` : 리액트에 필요한 아이콘 
- react-player 설치 `npm install react-player` : 유튜브 영상 재생
- sass 설치 `npm install sass` : CSS 라이브러리
- react-helmet-asyne 설치 `npm install react-helmet-async` : SEO
- swiper 설치 `npm install swiper` : 이미지 슬라이트




## 트러블 슈팅
- node.js 설치 시 폴더 인식 못함:
검색을 해보니~~~~ 이렇게 해결했다


## JSX 파일
JSX 파일은 JavaScript XML의 약자이며, 주로 React 애플리케이션에서 사용되는 확장자입니다. JSX는 JavaScript와 XML을 조합한 문법으로, JavaScript 코드 내에 마크업을 작성할 수 있게 해줍니다. 이는 React 컴포넌트를 선언하고 UI를 정의하는데 사용됩니다.

JSX 파일은 일반적으로 .jsx 확장자를 가지며, 내부적으로는 JavaScript 코드로 변환되어 실행됩니다. JSX를 사용하면 JavaScript 코드를 더욱 가독성 있고 유지보수하기 쉽게 만들어줍니다. 또한 JSX를 사용하면 UI를 선언적으로 정의할 수 있으며, JavaScript의 기능을 활용하여 동적으로 UI를 조작할 수 있습니다.

예를 들어, 다음은 간단한 React 컴포넌트를 정의하는 JSX 파일의 예시입니다:

````jsx
Copy code
// HelloWorld.jsx

import React from 'react';

function HelloWorld(props) {
  return (
    <div>
      <h1>Hello, {props.name}!</h1>
      <p>Welcome to my React application.</p>
    </div>
  );
}
````

export default HelloWorld;
위 코드에서 &lt;div&gt;와 &lt;h1&gt; 등의 태그는 HTML과 유사하게 보이지만, 실제로는 JavaScript 코드입니다. JSX 파일은 이러한 형태로 작성되며, Babel과 같은 도구를 사용하여 일반 JavaScript 코드로 변환됩니다.

## Home.jsx 폴더에서
단축키_ rafce   
- "rafc"는 React 함수형 컴포넌트를 자동으로 생성하는 Visual Studio Code의 단축키입니다. 이는 React 개발을 더욱 효율적으로 만들어주는 기능 중 하나입니다. "rafc"를 입력하고 엔터 키를 누르면 다음과 같은 코드가 자동으로 생성됩니다.
- &lt;div&gt;와 &lt;div&gt; 안에 폴더 이름 넣어주기

````jsx
jsx
Copy code
import React from 'react'

export default function ComponentName() {
    return (
        <div>
            
        </div>
    )
}
````

위 코드에서 "ComponentName"은 사용자가 지정한 컴포넌트의 이름을 의미합니다. 이 기능은 React 개발을 빠르고 효율적으로 만들어주며, 컴포넌트를 생성할 때 반복되는 구조를 줄여줍니다.


## 페이지 잘 만들어졌는지 확인하는 법
- 터미널 실행
- npm start 입력
- http://localhost:3000/ 확인
- 브라우저 열고 localhost:3000/해당 폴더이름 입력
- 브라우저 열고 localhost:3000/Home

## scss 페이지 잘 만들어졌는지 확인하는 법
- scss 폴더 만들기
- 새로운 터미널 만들기
- npm run build //입력

- ##





