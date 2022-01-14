---
layout: post
title: Place-n-Piece (현재 진행중)
description: >
  Place-n-Piece (현재 진행중)
sitemap: false
hide_last_modified: false
categories:
  - project
---

# Place n Piece (현재 진행중)

<style>

#modalLayer {
  z-index: 500;
  position: fixed;
  background: rgba(0, 0, 0, 0.8);
  width: 100%;
  height: 100%;
  top: 0;
  left: 0;
}

.modalBox {
  width: 81%;
  height: auto;
  position: relative;
  text-align: center;
  left: 7.5%;
  top: 0;
  position: sticky;
  margin: 0;
  margin-top: 1.5%
}

.modalImg {
  display: block;
}

.btnBox {
  position: relative;
  left: 7.5%;
  width: 81%;
  height: auto;
}

#closeButton {
  display: block;
  float: right;
}

#closeButton:hover {
  cursor: pointer;
}

.slickImg:hover {
  cursor: -webkit-zoom-in;
}

.modalImg:hover {
  cursor: grabbing;
}

</style>

<script>
  $(document).ready(function() {
    $('.main_center').slick({
      autoplay : true, /*자동으로 슬라이딩됨*/
      dots : true, /* 하단 점 버튼 */
      speed : 700, /* 이미지가 슬라이딩시 걸리는 시간 */
      infinite : true,
      autoplaySpeed : 5000, /* 이미지가 다른 이미지로 넘어 갈때의 텀 */
      arrows : true,
      slidesToShow : 1,
      slidesToScroll : 1,
      touchMove : false, /* 마우스 클릭으로 끌어서 슬라이딩 가능여부 */
      nextArrows : true, /* 넥스트버튼 */
      prevArrows : true,
      arrow : true, /*false면 좌우 버튼 없음, true면 좌우 버튼 보임*/
      fade : false
    });
  });

  function modal () {
    const modLayerElem = document.querySelector("#modalLayer");
    const modBox = document.querySelector(".modalBox");
    const modImg = document.querySelector(".modalImg");
    modLayerElem.style.display = "block";

    $(function(){
      $('.modalBox').slick({
      autoplay : false, /*자동으로 슬라이딩됨*/
      dots : true, /* 하단 점 버튼 */
      speed : 700, /* 이미지가 슬라이딩시 걸리는 시간 */
      infinite : true,
      autoplaySpeed : 5000, /* 이미지가 다른 이미지로 넘어 갈때의 텀 */
      arrows : true,
      slidesToShow : 1,
      slidesToScroll : 1,
      touchMove : true, /* 마우스 클릭으로 끌어서 슬라이딩 가능여부 */
      nextArrows : true, /* 넥스트버튼 */
      prevArrows : true,
      arrow : true, /*false면 좌우 버튼 없음, true면 좌우 버튼 보임*/
      fade : false
      });
    });
  };

  function modClose () {
    const modLayerElem = document.querySelector("#modalLayer");
    modLayerElem.style.display = "none";
  }
</script>

- toc
{:toc .large-only}

🔎 About 　　　　　　실제 장소(카페, 전망 좋은 위치 등)를 Web-App 으로 구현하여 가상 장소를 제공
　　　　　　　　　　 하고 그날의 기분, 일기, 방명록, 유저 커뮤니케이션 등의 컨텐츠를 제공하여 가상
　　　　　　　　　　 장소를 실제로 방문한듯한 User Experience 를 서비스 하는 메타버스 플랫폼  \
　 \
📅 프로젝트 기간 　　 &nbsp;2021/01/11 ~ 진행중 \
　 \
👨🏽‍🤝‍👨🏻 팀원　　　　　　　 개인 프로젝트, 추후 팀원 모집 계획중 \
　 \
💡 담당 Stack 　　　　&nbsp;`React` `Redux` \
 \
🏢 활동 소속　　　　 &nbsp; 프로젝트인원 모집 계획중

---

<div class="main_center">

</div>

## Content

> 현재 개발중에 있으며, 빠른 시일내에 Example Project 형태로 배포할 계획입니다.   \
> **User Communication** 형성과 좋은 **User Experience** 를 경험하도록 개발하고 싶습니다.   \
> 리액트를 다루는 기술 ( 김민준 / velopert 저 ) 에서 만드는 Blog Project 에서 나만의 프로젝트로 특색있게 만들고자 생각 하다가 떠오른 아이디어 에서 출발한 프로젝트 입니다.    \
> 자세한 기획 내용에 관심이 생기셨다면 **[노션 링크](https://www.notion.so/f52736647b8741328d8194ce78fade7a)**를 확인해주시기 바랍니다.    \
> 또한 가능한 선에서 최신 기법으로 개발하려고 노력하고 있습니다.

## Link

- **[Code (github)](https://github.com/steven-yn/Place-n-Piece)**
- **[노션](https://www.notion.so/f52736647b8741328d8194ce78fade7a)**

## Demo

준비중

## Stacks

- Framework : `React(FE)` `Node.js(BE)`
- Library : `Redux(Saga)` `@emotion/react` `Babel` `Axios` `Koa` `mongoose` `bcrypt` `JWT`
- Package : `Yarn` `webpack`
- Database : `MongoDB`
- Server Hosting : `AWS EC2`
- Main Language : `Javascript`

## 담당 기능 (Full-Stack)

- CSS-in-JS (@emotion/react) 를 이용하여 작업
  + 높은 재사용성 Component 설계
  + 시맨틱한 마크업, 반응형 UI 를 위함
- Component (UI, Container, Redux)
- 비동기 작업 처리 (Redux-Saga, Axios)
- 가능한한 UX 에 초점을 맞춘 front-end 개발

## 도입 예정 Stack

- 퍼블리싱 및 UI 관련 전반적인 기술 (미디어 쿼리, SEO, 크로스 브라우징)
- 대형 트래픽 솔루션 (immer, memo, SSR...)
- React@v18 업그레이드 예정인 Suspense 사용예정
- Typescript 사용
- Rest API 설계 및 백엔드 와의 데이터 HTTP 통신
  + 집중적으로 연구 개발

<div id="modalLayer" style="display: none">
<div>
