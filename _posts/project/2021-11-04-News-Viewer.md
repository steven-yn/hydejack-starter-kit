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

<img src="/assets/img/project/News-Viewer/mainPage.jpg" width="" height="" title="메인(전체보기) 페이지" alt = ""> | <img src="/assets/img/project/News-Viewer/waitPage.jpg" width="" height="" title="대기 페이지" alt = "">

<img src="/assets/img/project/News-Viewer/sportsPage.jpg"> | <img src="/assets/img/project/News-Viewer/newsPage.jpg" width="" height="" title="관리자 페이지" alt = "">

> <mark>News-Viewer</mark> 는 뉴스 API 를 받아와 렌더링하는 어플리케이션 입니다. \
> 기본적으로 메인 페이지에서 카테고리에 상관없이 **전체보기** 로 뉴스를 보고, **카테고리**에 따라 관련 기사들을 볼수 있으며, 기사를 클릭하면 해당 기사를 발행한 신문사 사이트로 이동합니다.

## Link

- **[Code (github)](https://github.com/steven-yn/News-Viewer)**

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
