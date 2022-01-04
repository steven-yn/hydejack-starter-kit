---
layout: about
image: /assets/img/me/me.jpg
description: >
  프론트엔드 개발을 공부하고 있습니다.
hide_description: true
---

<!--author-->

---

<style>
  .container {
    margin: 20px !important;
  }

  .list {
    display: flex !important;
    flex-wrap: wrap !important;
    flex-direction: column !important;
  }

  .list .left-at-scroll {
    margin-top: 20px !important;
    transition: transform 1.5s, opacity 1s !important;
  }

  .list .up-at-scroll {
    margin-top: 20px !important;
    transition: transform 1.5s, opactity 1s !important;
  }

  .list .bar-scroll {
    margin-top: 20px !important;
    transition: transform 0.7s, opacity 0.7s !important;
  }


  .bar-container {
    float: left;
    width: 100%;
    background-color: #f1f1f1;
    text-align: center;
    color: white;
    border-radius: 15px;
    margin-top: 2px;
  }

  .bar {
    width: 1%;
    height: 1.5rem;
    border-radius: 15px;
    display: flex;
    align-items: center;   
  }

</style>

<script>
  function isElementUnderBottom(elem, triggerDiff) {
    const { top } = elem.getBoundingClientRect();
    const { innerHeight } = window;
    return top > innerHeight + (triggerDiff || 0);
  }

  function handleScroll() {
    const xelems = document.querySelectorAll('.left-at-scroll');
    const yelems = document.querySelectorAll('.up-at-scroll');
    const barElems = document.querySelectorAll('.bar-scroll');
    const bbarElems = document.querySelectorAll(".bar");

    xelems.forEach(elem => {
      if (isElementUnderBottom(elem, -100)) {
        elem.style.opacity = "0";
        elem.style.transform = 'translateX(-100px)';

      } else {
        elem.style.opacity = "1";
        elem.style.transform = 'translateX(0px)';
      }
    })

    yelems.forEach(elem => {
      if (isElementUnderBottom(elem, -100)) {
        elem.style.opacity = "0";
        elem.style.transform = 'translateY(-100px)';

      } else {
        elem.style.opacity = "1";
        elem.style.transform = 'translateY(0px)';
      }
    })

    barElems.forEach(elem => {
      if (isElementUnderBottom(elem, 50)) {
        elem.style.opacity = "0";
        elem.style.transform = 'translateX(-20px)';

      } else if (elem.style.opacity === "1") {

        elem.addEventListener('transitionrun', move);

        function move() {
          bbarElems.forEach(eelem => {
            if (eelem.style.width < "2%") {
              let width = 1;
              let sum = 1;
              
              var id = setInterval(frame, 7);
              const barper = eelem.querySelector(".barper").innerText;

              function frame() {
              if (width >= 99) {
                  clearInterval(id);
              } else {
                  width++;
                  const perwidth = barper / 100;
                  sum += perwidth;
                  eelem.style.width = sum +'%';
              }
              }
            }
          })
        }

      } else {
        elem.style.opacity = "1";
        elem.style.transform = 'translateX(0px)';
        
      }
    })
  }

  window.addEventListener('scroll', handleScroll);
</script>

<center>
<span style="font-size:170%;font-weight:bold"> 윤성연
</span>
</center>
<center>MAJOR : Semi-Conductor</center>
<center>Chung-Ju University</center>
<center>31, haeyang-ro, Sangrok-gu, Kyung-gi, Republic of Korea</center>

<div class="container">
  <div class="list">
    <article class="left-at-scroll">
      <h2 id="personal-data">
        Personal Data
      </h2>
      <hr>
    </article>

    <article class="left-at-scroll">
      <blockquote>
        1994.10.09 (29) 대한민국, 인천 시, 남구 출생 <br>
        지역 : 경기도 안산시 상록구 <br>
        관심 개발분야 : 프론트엔드, 퍼블리싱, 웹 크롤링, 데이터활용 UI, 펌웨어
      </blockquote>
    </article>

    <article class="left-at-scroll">
      <h2 id="major-class">
        Major Class
      </h2>
      <hr>
    </article>

    <article class="left-at-scroll">
      <blockquote>
        <strong>
        융합전자공학부 (DIVISION OF ELECTRONIC ENGINEERING) <br>
        </strong>
        <br>
        <ul>
          <li>
            회로이론 / 전자회로 / 전기수학
          </li>
          <li>
            C언어 / 마이크로 프로세서 / 캡스톤 디자인 (자유주제: 드론설계)
          </li>
          <li>
            논리회로 / VHDL / Verilog / SoC 설계
          </li>
          <li>
            반도체 소자공학 / 반도체 공정 / RF 공학
          </li>
          <li>
            TCAD / 디지털집적회로
          </li>
        </ul>
      </blockquote>
    </article>

    <article class="left-at-scroll">
      <h2 id="license">
        License
      </h2>
      <hr>
    </article>

    <article class="left-at-scroll">
      <blockquote>
        <ul>
          <li>
            웹디자인 기능사
          </li>
          <li>
            ITQ 엑셀 A급
          </li>
          <li>
            운전면허1종보통
          </li>
        </ul>
      </blockquote>
    </article>

    <article class="left-at-scroll">
      <h2 id="history">
        History
      </h2>
      <hr>
    </article>

    <article class="up-at-scroll">
      <div class='list-post'>
        <h2 id="now" class="list-lead">
            현재
        </h2>
        <ul class="related-posts">
          <li class="h6">
            <div>
              <time style="display: inline-block; width: 2.2rem" class="faded fine" datetime="2021-11-29T00:00:00+09:00">2021.06　 2021.11</time>
              <a href="#" class="flip-title">
              </a>
              <span style="margin-left: 5rem">
                파이썬과 R을 활용한 빅데이터 UI 개발자
              </span>
            </div>
          </li>
          <li class="h6">
            <div>
              <time style="display: inline-block; width: 2.2rem" class="faded fine" datetime="2021-06-15T00:00:00+09:00"></time>
              <span style="margin-left: 7rem">
                ( 안산이젠컴퓨터학원 )
              </span>
            </div>
          </li>
          <li class="h6">
            <div>
              <time style="display: inline-block; width: 2.2rem" class="faded fine" datetime="2021-04-30T00:00:00+09:00">2021.02　 2021.04</time>
              <a href="#" class="flip-title">
              </a>
              <span style="margin-left: 5rem">
                Neo Health Technology
              </span>
            </div>
          </li>
          <li class="h6">
            <div>
              <time style="display: inline-block; width: 2.2rem" class="faded fine" datetime="2021-02-03T00:00:00+09:00"></time>
              <span style="margin-left: 7rem">
                ( Resercher, Hardware / VHDL - Cyclone V, Platform Designer, NIOS II )
              </span>
            </div>
          </li>
          <li class="h6">
            <div>
              <time style="display: inline-block; width: 2.2rem" class="faded fine" datetime="2021-02-13T00:00:00+09:00">2017.09　 2021.02</time>
              <a href="#" class="flip-title">
              </a>
              <span style="margin-left: 5rem">
                청주대학교 졸업
              </span>
            </div>
          </li>
          <li class="h6">
            <div>
              <time style="display: inline-block; width: 2.2rem" class="faded fine" datetime="2017-09-01T00:00:00+09:00"></time>
              <span style="margin-left: 7rem">
                ( 성적장학금 4회 중 최우수 1회, 졸업작품 : 라즈베리파이를 활용한 드론설계(자유주제) )
              </span>
            </div>
          </li>
          <li class="h6">
            <div>
              <time style="display: inline-block; width: 2.2rem" class="faded fine" datetime="2017-04-13T00:00:00+09:00">2017.04　 2015.07</time>
              <a href="#" class="flip-title">
              </a>
              <span style="margin-left: 5rem">
                육군 만기전역
              </span>
            </div>
          </li>
          <li class="h6">
            <div>
              <time style="display: inline-block; width: 2.2rem" class="faded fine" datetime="2015-07-13T00:00:00+09:00"></time>
              <span style="margin-left: 7rem">
                ( 강원도 화천, 2포병여단, 운전병 )
              </span>
            </div>
          </li>
          <li class="h6">
            <div>
              <time style="display: inline-block; width: 2.2rem" class="faded fine" datetime="2015-07-13T00:00:00+09:00">2014.07　 2015.07</time>
              <a href="#" class="flip-title">
              </a>
              <span style="margin-left: 5rem">
                청주대학교 입학
              </span>
            </div>
          </li>
          <li class="h6">
            <div>
              <time style="display: inline-block; width: 2.2rem" class="faded fine" datetime="2014-03-02T00:00:00+09:00"></time>
              <span style="margin-left: 7rem">
                ( 1학년 2학기 휴학 )
              </span>
            </div>
          </li>
          <li class="h6">
            <div>
              <time style="display: inline-block; width: 2.2rem" class="faded fine" datetime="2013-02-00T00:00:00+09:00">2010.03　 2013.02</time>
              <a href="#" class="flip-title">
              </a>
              <span style="margin-left: 5rem">
                양지고등학교 졸업
              </span>
            </div>
          </li>
          <li class="h6">
            <div>
              <time style="display: inline-block; width: 2.2rem" class="faded fine" datetime="2010-03-00T00:00:00+09:00"></time>
              <span style="margin-left: 7rem">
                ( 인문계 이과 계열 )
              </span>
            </div>
          </li>
        </ul>
      </div>
    </article>

    <article class="left-at-scroll">
      <h2 id="skills">
        Skills
      </h2>
      <hr>
    </article>

    <article class="bar-scroll">
      <blockquote>
        <ul>
          <li>
            <strong>Language</strong> : <code class="language-plaintext highlighter-rouge">Javascript</code>, <code class="language-plaintext highlighter-rouge">HTML</code>, <code class="language-plaintext highlighter-rouge">CSS</code>, <code class="language-plaintext highlighter-rouge">C</code>, <code class="language-plaintext highlighter-rouge">VHDL</code>
            <ul>
              <li style="">
                <div class="bar-container">
                  <div id="Content_bar" class="bar" style="background-color: #ffdf51;"><span class="font-hl" style=" padding: 0 5px 0 7px">Javascript : <span class="barper">40</span>%</span></div>
                </div>
              </li>

              <li>
                <div class="bar-container">
                  <div id="Content_bar" class="bar" style="background-color: skyblue;"><span class="font-hl" style="color: white; padding: 0 5px 0 5px">HTML / CSS : <span class="barper">50</span>%</span></div>
                </div>
              </li>

              <li>
                <div class="bar-container">
                  <div id="Content_bar" class="bar" style="background-color: #9a2ace;"><span class="font-hl" style="color: white">C : <span class="barper">50</span>%</span></div>
                </div>
              </li>

              <li>
                <div class="bar-container">
                  <div id="Content_bar" class="bar" style="background-color: darkblue;"><span class="font-hl" style="color: white">VHDL : <span class="barper">35</span>%</span></div>
                </div>
              </li>
            </ul>
          </li>
        </ul>
      </blockquote>
    </article>

    <article class="bar-scroll">
      <blockquote>
        <ul>
          <li>
            <strong>FrameWork</strong> : <code class="language-plaintext highlighter-rouge">React</code>, <code class="language-plaintext highlighter-rouge">Node.js</code>
            <ul>
              <li>
                <div class="bar-container">
                  <div id="Content_bar" class="bar" style="background-color: #4ee0f3;"><span class="font-hl" style="color: white">React : <span class="barper">40</span>%</span></div>
                </div>
              </li>

              <li>
                <div class="bar-container">
                  <div id="Content_bar" class="bar" style="background-color: limegreen;"><span class="font-hl" style="color: white">Node.js : <span class="barper">20</span>%</span></div>
                </div>
              </li>
            </ul>
          </li>
        </ul>
      </blockquote>
    </article>

    <article class="bar-scroll">
      <blockquote>
        <ul>
          <li>
            <strong>Library</strong> : <code class="language-plaintext highlighter-rouge">Redux</code>, <code class="language-plaintext highlighter-rouge">JQuery</code>
            <ul>
              <li>
                <div class="bar-container">
                  <div id="Content_bar" class="bar" style="background-color: mediumpurple;"><span class="font-hl" style="color: white">Redux : <span class="barper">35</span>%</span></div>
                </div>
              </li>

              <li>
                <div class="bar-container">
                  <div id="Content_bar" class="bar" style="background-color: sienna;"><span class="font-hl" style="color: white;  padding: 0 5px 0 7px">JQuery : <span class="barper">25</span>%</span></div>
                </div>
              </li>
            </ul>
          </li>
        </ul>
      </blockquote>
    </article>

    <article class="left-at-scroll">
      <blockquote>
        <ul>
          <li>
            <strong>Software / OS</strong> : <code class="language-plaintext highlighter-rouge">Git</code>, <code class="language-plaintext highlighter-rouge">Linux</code>, <code class="language-plaintext highlighter-rouge">AWS-EC2</code>
          </li>
        </ul>
      </blockquote>
    </article>

  </div>
</div>
