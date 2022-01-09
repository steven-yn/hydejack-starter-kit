---
layout: post
title: Web-Design-Crafter
description: >

sitemap: false
hide_last_modified: false
categories:
  - project
---

# 웹디자인기능사

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

🔎 About 　　　　　　 HTML, CSS, jQuery 로 이루어진 퍼블리싱 역량을 확인하는 시험입니다. \
　 \
📅 프로젝트 기간 　　 &nbsp;2021/10/22 ~ 2021/12/13 \
　 \
👨🏽‍🤝‍👨🏻 팀원　　　　　　　 개인 자격증 시험 \
　 \
💡 사용 Stack 　　　　&nbsp;`HTML5` `CSS3` `jQuery`

---

## Content

<div class="main_center">
    <div><img class="slickImg" src="/assets/img/project/Crafter/layout.jpg" style="width: auto; height: 500px; margin: 0 auto;" onClick="modal()" title="레이아웃 잡기"></div>
    <div><img class="slickImg" src="/assets/img/project/Crafter/slideImg.jpg" style="width: auto; height: 500px; margin: 0 auto;" onClick="modal()" title="메인 슬라이드 배너"></div>
    <div><img class="slickImg" src="/assets/img/project/Crafter/slideMenu.jpg" style="width: auto; height: 500px; margin: 0 auto;" onClick="modal()" title="슬라이드형 메뉴"></div>
    <div><img class="slickImg" src="/assets/img/project/Crafter/modal.jpg" style="width: auto; height: 500px; margin: 0 auto;" onClick="modal()" title="모달"></div>
</div>
<script>
    $(document).ready(function() {
        $('.main_center').slick({
            autoplay : true, /*자동으로 슬라이딩됨*/
            dots : true, /* 하단 점 버튼 */
            speed : 700 /* 이미지가 슬라이딩시 걸리는 시간 */,
            infinite : true,
            autoplaySpeed : 5000 /* 이미지가 다른 이미지로 넘어 갈때의 텀 */,
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
</script>

> 웹디자인 기능사 실기 준비시 공개문제를 연습했던 프로젝트들 입니다.

## Link

- **[Code (github)](https://github.com/steven-yn/Web-Design-Crafter)**

## Demo

준비중

## Stacks

- Library : `jQuery`

## 개발당시 느낀점들

> 퍼블리싱에 대한 이해도가 전혀 없었을때 공부했던 내용입니다.
> 시험을 준비하면서 html 요소나 css 스타일링을 해보면서 퍼블리싱 숙련도를 올렸습니다.
> 또한 jQuery를 다루면서 dom 을 쉽게 접근해서 동적인 페이지를 제작할수 있었습니다.
> 저에게는 프론트엔드에 입문하게 해준 첫 프로젝트 라고 할수 있습니다.

<div id="modalLayer" style="display: none">
  <div class="modalBox">
    <div><img class="modalImg" src= "/assets/img/project/Crafter/layout.jpg" style="width: auto; height: auto; margin: 0 auto;" title="레이아웃 잡기"></div>
    <div><img class="modalImg" src= "/assets/img/project/Crafter/slideImg.jpg" style="width: auto; height: auto; margin: 0 auto;" title="메인 슬라이드 배너"></div>
    <div><img class="modalImg" src= "/assets/img/project/Crafter/slideMenu.jpg" style="width: auto; height: auto; margin: 0 auto;" title="슬라이드형 메뉴"></div>
    <div><img class="modalImg" src= "/assets/img/project/Crafter/modal.jpg" style="width: auto; height: auto; margin: 0 auto;" title="모달"></div>
  </div>
  <div class="btnBox">
    <span id="closeButton" onClick="modClose()" style="width: auto; height: auto; border: solid 1px; border-radius: 5px; padding: 5px 10px 5px 10px; color: white">
      닫기
    </span>
  </div>
<div>
