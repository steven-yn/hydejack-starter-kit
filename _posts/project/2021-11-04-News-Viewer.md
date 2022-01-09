---
layout: post
title: News-Viewer
description: >

sitemap: false
hide_last_modified: false
categories:
  - project
---

# News-Viewer with React

- toc
{:toc .large-only}

🔎 About 　　　　　　리액트로 개발한 News를 불러오고 볼수있는 어플리케이션 입니다. \
　 \
📅 프로젝트 기간 　　 &nbsp;2021/10/30 ~ 2021/11/2 \
　 \
👨🏽‍🤝‍👨🏻 팀원　　　　　　　 개인 사이드 프로젝트 \
　 \
💡 사용 Stack 　　　　&nbsp;`React` `react-router-dom` `Axios` `Custom-Hooks` `Styled-Componets`

---

## Content

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

<div class="main_center">
    <div><img class="slickImg" src= "/assets/img/project/News-Viewer/mainPage.jpg" style="width: auto; height: 500px; margin: 0 auto;" title="메인(전체보기) 페이지" onClick="modal()"></div>
    <div><img class="slickImg" src="/assets/img/project/News-Viewer/waitPage.jpg" style="width: auto; height: 500px; margin: 0 auto;" title="대기 페이지" onClick="modal()"></div>
    <div><img class="slickImg" src= "/assets/img/project/News-Viewer/sportsPage.jpg" style="width: auto; height: 500px; margin: 0 auto;" title="스포츠 카테고리" onClick="modal()"></div>
    <div><img class="slickImg" src= "/assets/img/project/News-Viewer/newsPage.jpg" style="width: auto; height: 500px; margin: 0 auto;" title="뉴스 클릭시 이동" onClick="modal()"></div>
</div>

> <mark>News-Viewer</mark> 는 뉴스 API 를 받아와 렌더링하는 어플리케이션 입니다. \
> 기본적으로 메인 페이지에서 카테고리에 상관없이 **전체보기** 로 뉴스를 보고, **카테고리**에 따라 관련 기사들을 볼수 있으며, 기사를 클릭하면 해당 기사를 발행한 신문사 사이트로 이동합니다.

## Link

- **[Code (github)](https://github.com/steven-yn/News-Viewer-React)**

## Demo

준비중
(`newsapi.org` 의 가격정책이 바뀐 이유로 브라우저로 바로 호출 할수 없게 됐습니다.)

## Stacks

- Framework : `React(FE)`
- Library : `Styled-Componets` `Axios` `Custom Component` `react-router-dom`
- Package : `Yarn` `webpack`

## 개발당시 느낀점들

> **외부 API** 를 가져와 사용하는것을 처음 해본 프로젝트 입니다.     \
> **JSON 형태**로 뉴스 정보를 받아와서 UI를 구성하고 데이터를 출력하는 형태입니다.      \
> API 호출 뿐만 아니라, **router** 와 호출시 발생하는 지연을 처리하는 **비동기 상태관리**에 대해서도      \
> 이해도를 높일수 있었습니다. 또한 주된 작업은 이런 데이터를 받아와서 **렌더링** 하는것임을 파악      \
> 할 수 있던 사이드 프로젝트 였습니다.

<div id="modalLayer" style="display: none">
  <div class="modalBox">
    <div><img class="modalImg" src= "/assets/img/project/News-Viewer/mainPage.jpg" style="width: auto; height: auto; margin: 0 auto;" title="메인(전체보기) 페이지"></div>
    <div><img class="modalImg" src="/assets/img/project/News-Viewer/waitPage.jpg" style="width: auto; height: auto; margin: 0 auto;" title="대기 페이지"></div>
    <div><img class="modalImg" src= "/assets/img/project/News-Viewer/sportsPage.jpg" style="width: auto; height: auto; margin: 0 auto;" title="스포츠 카테고리"></div>
    <div><img class="modalImg" src= "/assets/img/project/News-Viewer/newsPage.jpg" style="width: auto; height: auto; margin: 0 auto;" title="뉴스 클릭시 이동"></div>
  </div>
  <div class="btnBox">
    <span id="closeButton" onClick="modClose()" style="width: auto; height: auto; border: solid 1px; border-radius: 5px; padding: 5px 10px 5px 10px; color: white">
      닫기
    </span>
  </div>
<div>
