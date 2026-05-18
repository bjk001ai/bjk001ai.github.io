---
layout: post
title: "Gatsby-blog 연결"
date: 2026-05-18
categories: blog
---

## [Gatsby-blog 연결](https://bjk001ai.github.io/gatsby-blog/)

# [GitHub Pages] React 만들어보기(Claude AI도움)
1. React 기초(무료 학습 ko.react.dev)
    - 컴포넌트 : 레고 블록처럼 UI를 조각으로 나누는 것
    - props : 컴포넌트에 데이터 전달하는 방법
    - useState : 버튼 클릭 등 상태 변화 관리
    - JSX : HTML처럼 생긴 React 문법
    - 유투브 공부 : "드림코딩 React"
2. Node.js 설치
    - nodejs.org 접속 > LTS > Node.js 24.15.0 다운받아서 설치(Windows Installer (.msi))
    - 버전확인(node -v)
    - npm권한 설정(powershell 을 관리자 권한으로)
        - Set-ExecutionPolicy -Scope CurrentUser -ExecutionPolicy RemoteSigned
    - npm -v
3. Gatsby CLI 설치
    - npm install -g gatsby-cli
    - gatsby --version
4. Gatsby 블로그 생성
    - gatsby new gatsby-blog https://github.com/gatsbyjs/gatsby-starter-blog
    - cd gatsby-blog
    - gatsby develop
    - http://localhost:8000 확인
5. GitHub에 올리기
    - GitHub에 새 Repository 만들기(gatsby-blog)
    - Gatsby GitHub Pages 플러그인 설치
        - npm install gh-pages --save-dev
    - gatsby-config.js에 pathPrefix 추가
        - pathPrefix: `/gatsby-blog`,
    - package.json 에 배포 스크립트 추가
        - VSCode에서 package.json 열고 "scripts" 부분에 "deploy" 한 줄 추가
        - "deploy": "gatsby build --prefix-paths && gh-pages -d public -b gh-pages",
    - GitHub 연결 후 배포
        - git init
        - git remote add origin https://github.com/bjk001ai/gatsby-blog.git
        - git add .
        - git commit -m "Gatsby 블로그 시작"
        - git push -u origin main
        - npm run deploy
    - GitHub Pages 설정
        - Repository → Settings → Pages → Branch를 gh-pages 로 변경 → Save!
6. 접속확인 및 글 올리기
    - https://bjk001ai.github.io/gatsby-blog/
    - content/blog 아래 폴더 만든후 index.md 만든어서 작성
    - 로컬확인(gatsby develop 명령어 입력후 localhost:8000 확인)
    - 글 수정후 npm run deploy