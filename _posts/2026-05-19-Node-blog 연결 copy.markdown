---
layout: post
title: "Node-blog 연결"
date: 2026-05-18 16:26:11 +0900
categories: blog
---

## [Node-blog 연결](https://bjk001ai.github.io/node-blog/)

#  [GitHub Pages] node.js(SSG) 만들어보기(Antigravity - Jemini Pro AI도움)
1. Node.js(LTS) 다운로드 (https://nodejs.org/dist/v24.15.0/node-v24.15.0-x64.msi)
2. 라이브러리 설치
    - npm install marked gray-matter
3. (AI한테 만들어달라고 부탁)
4. content/posts/ 폴더에 마크다운(.md) 파일로 글을 작성
5. 로컬빌드 : Node.js 스크립트(src/build.js)가 dist에 html로 변환
    - $ export BASE_URL="/dist/"
    - npm run build
6. 미리보기
    - npm run admin 를 치면 입력할수 있는 창이 나옴
    - npm run preview 미리 보기할수 있음
    - dist/index.html 오른쪽 마우스 Open With Live Server로 미리보기 할수 있음
7. 자동 배포 (GitHub Actions): 코드를 GitHub에 Push하면, GitHub 서버가 알아서 Node.js 스크립트를 실행