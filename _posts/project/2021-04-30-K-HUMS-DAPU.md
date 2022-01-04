---
layout: post
title:
description: >
  수리온 K-HUMS DAPU 국방과제
sitemap: false
hide_last_modified: false
categories:
  - project
---

# K-HUMS 국방과제

* toc
{:toc .large-only}

🔎 About 　　　　　　근무기간 동안 참여한 KHUMS 국가과제 입니다.  \
　 \
📅 프로젝트 기간 　　 &nbsp;2021/02/03 ~ 2020/4/30 \
　 \
👨🏽‍🤝‍👨🏻 팀원　　　　　　　프로젝트 총괄 1명, FPGA 코딩 및 하드웨어 1명 \
　 \
💡 담당 Stack 　　　　&nbsp;`FPGA` `Platform Designer` `NIOS II` `C` `Driver` \
 \
🏢 활동 소속　　　　 &nbsp;네오헬스테크널러지 (NHT)

---

## Content

<div class="main_center">
    <div><img src= "/assets/img/project/KHUMS/HUMS.jpg" style="width: auto; height: 400px; margin: 0 auto;" title="HUMS 개요"></div>
    <div><img src= "/assets/img/project/KHUMS/VHDL.jpg" style="width: auto; height: 400px; margin: 0 auto;" title="Quartus VHDL"></div>
    <div><img src= "/assets/img/project/KHUMS/Pin-Assign.jpg" style="width: auto; height: 400px; margin: 0 auto;" title="HUMS 개요"></div>
    <div><img src= "/assets/img/project/KHUMS/Plat-Desi.jpg" style="width: auto; height: 400px; margin: 0 auto;" title="HUMS 개요"></div>
    <div><img src= "/assets/img/project/KHUMS/NIOS-II-firm.jpg" style="width: auto; height: 400px; margin: 0 auto;" title="HUMS 개요"></div>
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

<mark> 위 이미지는 실제 프로젝트 참여 이미지가 아닌 참고용 이미지 임을 알립니다. </mark>

> <mark>KHUMS</mark> 국가과제는 HUMS 국산화 프로젝트 입니다.      \
> HUMS 에 들어가는 SRU 중, DPU 와 APU 개발 파트 였습니다.      \
> DPU 는 디지털 신호처리를, APU 는 아날로그 신호 처리를 담당합니다.      \
> 자세한 내용은 국방과제 이므로 비공개 보안 사항 입니다.

## Stacks

- FPGA : `Cyclone V`
- OS : `NIOS II`
- `SRAM` `DDR3` `Flash Memory` `ADC` `PCIe` `RS485` `SPI` `Shift Register`

## 담당 기능 (Full-Stack)

- MCU 의 역할을 할수 있도록 FPGA 를 설계. (Main Board, Core)
- FPGA 에서 NIOS II가 구동될수 있도록 Platform Designer 설계
- 각 하드웨어 들이 작동하는지 NIOS 및 Quartus 상에서 디버깅, 검증
- 잘못된 회로나 FPGA Pin Assignment 검증

## 개발당시 느낀점들

> 졸업 하기 2주전쯤 입사하고, 입사 하자마자 **바로 투입**됐던 프로젝트 입니다.      \
> 개발에 바로 투입되기에는 실력이 많이 모자랐지만, 실무에 참여해보고 싶었던 참이라 공부 해가며 개발했었습니다.     \
> **ASIC 용 칩 설계**에만 사용되는줄 알았던 FPGA 로 **MCU와 같은 역할**을 하도록 설계 하는 업무가 주됬었습니다.      \
> **Memory 칩 들을 Assign** 하는 작업이나, **ADC 칩을 Spec 에 맞게 Assign** 하는 작업들을 하면서 컴퓨터 구조에 대해 좀더 깊이 이해하게 되었고, 이를 **가상 OS인 NIOS** 에 올려 MCU 로써 작동하는 것을 경험 했습니다.      \
> NIOS 에서 C 언어로 된 **펌웨어 코드**들을 보면서 **구조를 파악**하는데 시간을 많이 들였는데, 생각보다 훨씬 **깊고 C 로 구조화 된 펌웨어**를 처음 봐서 많이 헤맸던 기억이 납니다.     \
> 당시 프로젝트를 진행하기엔 실력이 너무 부족했고, 이런것들을 배울기회는 너무 적고 혼자 공부하고있던 입장이었는데, 현재의 웹 개발 시장처럼 **정보공유 문화**가 부족한 분야라고 많이 느꼇습니다. 그래서 퇴사후 **웹 개발**을 시작하게된 계기가 됐습니다.
