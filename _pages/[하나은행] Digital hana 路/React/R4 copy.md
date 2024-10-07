---
title: "React"
tags:
    - 리액트
date: "2024-09-30"
thumbnail: "/assets/img/thumbnail/react.jpg"
bookmark: true
---

#  리액트
---

### 깃허브로 페이지 배포(간단히)

master 브런치로 이동하여서(당연히 dev꺼를 add, 커밋해두고!)
merge를 해서 dev브런치꺼를 합쳐둔다!!


그리고 설치

```shell
공통 (배포 전)
$> yarn add gh-pages -D            # npm i gh-pages -D
package.json > script > "deploy": "gh-pages -d dist",   추가!
```

```
추가설정
Deploying to https://<USERNAME>.github.io/<REPO>
# 1. vite.config.ts에서 base 설정
export default defineConfig({
  plugins: [react()],
  base: '/<REPO>/',                 // ex. base: '/hana4/',
});

# 1. main.tsx > BrowserRouter →→ HashRouter  // github은 try_files를 줄 수 없으므로 #으로 링크!
# 2. add & commit into master(main) branch
# 3. run build & deploy
$> yarn build            # npm run build vite build
$> yarn deploy           # https://indiflex.github.io/hana4   // 브라우저 cache면 쿠키 제거!
https://<github-id>.github.io/<repository>

Cf. git push -f git@github.com:indiflex/hana4.git main:gh-pages


```

깃허브 해당 리파지토리 폴더에 들어가서
세팅-> Pages -> 브런치 선택(gh-pages) ->완료



### stroybook/스토리북

```shell
storybook.js.org
$> npx storybook@latest init
$> yarn storybook

```