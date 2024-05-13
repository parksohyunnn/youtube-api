# Youtube API를 이용한 뷰티 사이트

## 작업 순서
1. node.js 설치 / 버전 확인
2. 폴더 셋팅 : 필요없는 파일 제거


## 필요한 라이브러리 설치
- react를 설치 `npm create-react-app 폴더이름` : 폴더를 생략하고 싶으면 .으로 표시
- react-router-dom 설치 `npm install react-router-dom` : 주소를 설정하기 위한 라이브러리
- axios 설치 `npm install axios` : API 라이브러리
- react icon 설치 `npm install react-icons` : 리액트에 필요한 아이콘 
- react-player 설치 `npm install react-player` : 유튜브 영상 재생
- sass 설치 `npm install sass` : CSS 라이브러리
- react-helmet-asyne 설치 `npm install react-helmet-async` : SEO
- swiper 설치 `npm install swiper` : 이미지 슬라이트


## 사용 스텍 
- node.js 설치


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
단축키_ rafc   
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





