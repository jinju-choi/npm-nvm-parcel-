npm 사용하기
# npm
`pakage.json`파일 생성
```bash
$ npm init -y
```

프로젝트에 해당하는 모든 **_모듈 설치_**
```bash
$ npm i
```

**_`dev`저장_**. 개발용으로만 활용되는 용도
```bash
$ npm install -D 번들러명
```

**_일반저장_**. 사이트가 동작하는데 필요한 용도
```bash
$ npm install 번들러명
```

# parcel bundler 사용
**_개발용_**
```bash
$ parcel index.html
```

**_사용자용_ 출력** 폴더가 생성 되고, 난독화 되어 생성.
```bash
$ parcel run build
$ parcel build index.html
```
***

`package.json`폴더 `scripts`에 명시 되어 있어야 한다.
```javascript
"scripts": {
    "dev": "parcel index.html",
    "build": "parcel build index.html"
  }
```

# npm Git 버전관리

`.gitignore` 파일 생성

```plaintext
.cache/
dist/
node_modules
```
버전관리 하지 않을 폴더명, 파일명을 입력한다.  
* `npm i`로 인해 생성된 파일과 `npm run build` 로 생성된 파일은 언제든 재생성이 가능하기 때문에 버전 관리를 하지 않는 것이 효율 적이다.


# nvm 버전매니저 사용법
node의 버전은 프로젝트에 따라 달라지기 때문에 nvm을 통해 여러가지 버전을 관리하는게 좋다.

_버전설치_
```bash
$ nvm install 버전
```

_버전삭제_
```bash
$ nvm uninstall 버전
```

_설치버전_ 확인
```bash
$ nvm --version
```

_설치 모든 된 버전_ 확인
```bash
$ nvm ls
```

_사용 버전 설정_
```bash
$ nvm use 버전
```

_버전 명령, 설명_
```bash
$ nvm --help 버전
```