---
layout: post
title:
description: >
  Raspi-Drone
sitemap: false
hide_last_modified: false
categories:
  - project
---

# RasberryPi-Drone

* toc
{:toc .large-only}

🔎 About 　　　　　　졸업작품 발표시 진행한 라즈베리파이를 활용한 드론설계 프로젝트 입니다. \
　 \
📅 프로젝트 기간 　　 &nbsp;2021/1/30 ~ 2020/12/20 \
　 \
👨🏽‍🤝‍👨🏻 팀원　　　　　　　개발 및 설계 1명, 설계 및 문서작업 1명 \
　 \
💡 담당 Stack 　　　　&nbsp;`디지털 회로 설계` `드론 비행 설계` `펌웨어 설계` `C` \
 \
🏢 활동 소속　　　　 &nbsp;청주대학교

---

## Content

<div class="main_center">
    <div><img src= "/assets/img/project/Raspi-FCC-And-Controller/fly-inside.jpg" style="width: auto; height: 500px; margin: 0 auto;" title="실내비행"></div>
    <div><img src="/assets/img/project/Raspi-FCC-And-Controller/ctrl.jpg" style="width: auto; height: 500px; margin: 0 auto;" title="컨트롤러"></div>
    <div><img src= "/assets/img/project/Raspi-FCC-And-Controller/Dev-Env.jpg" style="width: auto; height: 500px; margin: 0 auto;" title="개발환경"></div>
    <div><img src= "/assets/img/project/Raspi-FCC-And-Controller/ESC-test.jpg" style="width: auto; height: 500px; margin: 0 auto;" title="ESC 단위실험"></div>
    <div><img src= "/assets/img/project/Raspi-FCC-And-Controller/Landing-Skid.jpg" style="width: auto; height: 500px; margin: 0 auto;" title="랜딩 스키드 제작"></div>
    <div><img src= "/assets/img/project/Raspi-FCC-And-Controller/IMU-Moter-test.jpg" style="width: auto; height: 500px; margin: 0 auto;" title="IMU-모터 연동실험"></div>
    <div><img src= "/assets/img/project/Raspi-FCC-And-Controller/Drone-Present.jpg" style="width: auto; height: 500px; margin: 0 auto;" title="졸업작품 출품"></div>
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

> 졸업작품 발표를 준비하며 설계했던 **라즈베리파이를 활용한 드론설계** 프로젝트 입니다.   \
> 라즈베리파이는 각각 Controller MCU 부, 드론의 MCU 역할을 하는 FCC MCU 부에 들어갑니다. \
> 라즈베리파이 두대는 서로 블루투스로 통신하며 조이스틱을 조작하면 컨트롤러는 FCC로 각각 해당하는 신호를 전송합니다.
> throttle up,down 과 비상정지, Rolling과 Pitching을 제어할수있도록 설계했습니다.

## Link

- **[Code (github)](https://github.com/steven-yn/Raspi-FCC-And-Controller)**

## Record

<img src= "/assets/img/project/Raspi-FCC-And-Controller/fly-inside-vd.gif" style="width: 600px; height: 500px; margin: 0 auto;" title="실내비행"> <br>

<img src= "/assets/img/project/Raspi-FCC-And-Controller/IMU-Moter-test-vd.gif" style="width:600px; height: 500px; margin: 0 auto;" title="IMU 단위실험"> <br>

<img src= "/assets/img/project/Raspi-FCC-And-Controller/fly-outside-night.gif" style="width:300px; height: 500px; margin: 0 auto;" title="첫 야외비행"> <img src= "/assets/img/project/Raspi-FCC-And-Controller/fly-outside-high.gif" style="width:300px; height: 500px; margin: 0 auto;" title="좀더 나아졌지만 실패..">

## Stacks

- 디지털 회로 설계 : `Drone 구동부` `컨트롤러 구동부`
- 전자 회로 설계 : `Drone 전원부` `컨트롤러 전원`
- 펌웨어 설계 : `RasberryPi` `FCC(Drone)` `Controller` \
`DriverCode(BNO_055)` `DriverCode(MCP_3008)` `DriverCode(BLHeli-32)`
- Library : `WiringPi` `pigpio` `WiringPiI2C` `wiringPiSPI` `bluetooth` `rfcomm` `socket`

## 담당 기능 (Full-Stack)

- 드론 비행 원리와 그에 맞는 출력을 낼수있는 추력설계, 비행설계(Pitching, Rolling, Yawing)
- 각 모듈들과 MCU 처럼 사용하는 RasberryPi 간 DriverCode 설계, 디지털 회로 설계
- 각 DriverCode 를 이용해 RasberryPi 에서 C언어로 펌웨어 설계
- ESC PWM, SPI 통신, I2C 통신, Serial 통신, Parallel 통신, 블루투스 소켓통신 펌웨어 설계
- 전원부 전압 강하 및 전류 안정 회로 설계

## 개발당시 느낀점들

> 제가 코딩을 해서 **프로젝트** 라는것을 처음 진행해본 프로젝트 였습니다.
> 당시 배우던 전공인 전자회로와 마이크로프로세서 에서 배운 **전공지식**을 가지고 시작했습니다.
> 하지만 막상 시작하니 **모르는게 정말많아** 필요한 공부량이 정말 많았던 프로젝트 였습니다.
> **C언어** 조차 제대로 모르는 상황에서, **라즈베리파이**를 접하고, **드론의 비행원리**를 공부해가며,
> 여러가지 **통신**과 **드라이버코드**, **디지털 신호제어**등을 하나씩 개발해 나갔습니다.
> 아무런 **뼈대없이** ~~맨땅에 헤딩~~을 했던 프로젝트로 저에게 큰 **터닝포인트**가 됐던 프로젝트입니다.  \
> 결국 시제품과 비슷할 정도로 **매끄러운 동작도, 제대로된 비행도 못한채로 끝났지만**,
> **펌웨어 실력향상**이나 **개발 역량**이 크게 늘어나는 시점이 되었다고 생각합니다.
> 이제 와서 생각해보는 것 이지만, 좀더 쉬운 방법이나 가이드라인을 따라 개발했다면.. 하는 생각을 하게됩니다. 아쉬움이 많이 남았었습니다. 다음에 꼭 다시 완성시켜보고 싶습니다.
