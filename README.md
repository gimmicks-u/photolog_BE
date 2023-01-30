# Photolog Server

**포토로그의 자세한 개발과정과 고민들은 [이곳](https://sequoia-dust-a86.notion.site/Photolog-9214843c6058451db83a338e3ad8ccdb)에서 확인하실 수 있습니다.**


## Photolog 서비스소개

![스크린샷 2022-12-30 오전 1 34 28](https://user-images.githubusercontent.com/59651691/209982466-94f975b7-2c34-47ad-aac6-c185535a49e8.png)


## 프로젝트 기간

- 22.12/12~ 22.12/29 (3주)   


![stack](https://user-images.githubusercontent.com/59651691/209982205-54b5b26c-bf26-4ec9-a753-2fcd6fcace25.png)


## 데모영상
<details>
<summary>로그인 디자인</summary>
<img style="max-width: 100%; height: auto;" src="https://user-images.githubusercontent.com/54767632/209975619-8b6fa303-4e39-4131-9b03-c096e46ad3c1.gif" >
</details>

<details>
<summary>로그인 폼</summary>
<img style="max-width: 100%; height: auto;" src="https://user-images.githubusercontent.com/54767632/209975626-684a1ac2-eb98-49c2-87be-e7e9df56ddf9.gif" >
</details>

<details>
<summary>인트로 페이지(인터랙션)</summary>
<img style="max-width: 100%; height: auto;" src="https://user-images.githubusercontent.com/59651691/210131630-6d50021e-764d-46eb-b3ee-6bab952307fc.gif" >
</details>

<details>
<summary>지도 사진게시판</summary>
<img style="max-width: 100%; height: auto;" src="https://user-images.githubusercontent.com/59651691/210131218-c90c1f98-310e-4da8-add9-024f9e7d2b21.gif" >
</details>

<details>
<summary>무한스크롤 사진 게시판</summary>
<img style="max-width: 100%; height: auto;" src="https://user-images.githubusercontent.com/59651691/210131167-11ab68c7-4157-453b-97db-793ff5938421.gif" >
</details>

<details>
<summary>마이 페이지 내 게시글 조회</summary>
<img style="max-width: 100%; height: auto;" src="https://user-images.githubusercontent.com/59651691/210131349-0f3c3e21-71e8-4352-9d05-0b13118a25b4.gif" >
</details>




## ERD
![ photolog](https://user-images.githubusercontent.com/59651691/209972265-6125fd89-ed40-409a-91b3-64302be05f7c.png)


## 기능

- 마이페이지 자신의 사진 게시물보기
- 위도 경도 기반 사진 게시판 검색
- hashtag 기반 검색
- CloudFront+AWS lambda 이미지 최적화
- nodemailer 임시 비밀번호 전송

## Code Convention

- Commit Convention 규약 (VSCode Git Emoji)

  + ✨ feat : 새로운 기능 추가  

  + 🔥 remove  : 기능 삭제  

  + 📝 docs : 문서 수정

  + 🐛 fix: 수정사항 발생시, 버그픽스

  + 🎨 style:  코드 포매팅, 세미콜론 누락 등 코드 변경이 없는 경우. 

  + ♻ refactor: 리팩토링. 

  + 🎉 init: 프로젝트 초기설정.  

  + 🚀 deploy: 배포관련 커밋. 

- Eslint, Prettier 적용

## Collaboration Tools

- Discord : 스크림장소 및 env 및 세팅법 빠르게 공유하는 용도
- Notion : 스크럼 일지기록, 이슈 발생 기록
- ErdCloud : ERD 공유 및 typeorm Entity 변환
- JIRA : Issue Tracking
- Figma : 디자인 시안 공유
- Swagger : API 문서 공유


## 👪 Contributors

<br />

| 별칭(이름)              | 담당 업무 |
| ----------------------- | --------- |
| :rocket: 익수              | BE (팀장)|
| :turtle: 재훈              | BE      |
| :dolphin: 동한             | FE      |
| :sunglasses: 상현          | FE      |
| :crystal_ball: 충우        | FE      |
| :hatched_chick: 채현       | FE      |


## Getting Stated

- git clone 명령어

```jsx
mkdir photolog_server
cd photolog_server
git clone {....Photolog_Server.git} .
npm install
vi .env.dev
vi .env.staging

cd ..
mkdir photolog_client
cd photolog_client
git clone {....Photolog_Client.git} .
npm install
vi .env

```

- Frontend env 파일 (.env)

```jsx
REACT_APP_KAKAOMAP_API_KEY= {YOUR_KAKAOMAP_API_KEY}
REACT_APP_API_BASE_URL= {YOUR_API_REQUEST_BASE_URL}
```

- Backend local env 파일 (.env.dev)

```jsx
DB_TYPE="mysql"
DB_HOST="localhost"
DB_PORT=3306
DB_USERNAME="root"
DB_PASSWORD= {YOUR LOCALHOST ROOT PASSWORD}
DB_DATABASE= "photolog"
```

- Backend staging env 파일 (.env.staging)

```jsx
DB_TYPE="mysql"
DB_HOST= {YOUR_RDS_HOST_NAME}
DB_PORT=3306
DB_USERNAME="admin"
DB_PASSWORD= {YOUR_RDS_PASSWORD}
DB_DATABASE= {YOUR_RDS_DATABASENAME}
```

- Backend env 공통 요소

```jsx
PORT={YOUR_NESTJS_PORT}

PASSWORD_HASH_SALT= {YOUR_BCRYPT_HASH_SALT}

S3_ACCESS_KEY_ID= {YOUR_S3_ACCESS_KEY_ID}
S3_SECRET_ACCESS_KEY= {YOUR_SECRET_ACCESS_KEY}
S3_BUCKET_NAME= {YOUR_S3_BUCKET_NAME}
S3_PRESIGNED_EXPIRES= {YOUR_PRESIGNED_EXPIRES_SECOND}
S3_IMAGE_LIMIT_CAPA= {YOUR_IMAGE_CAPABILITY_MB}

ACCESS_SECRET= {YOUR_JWT_ACCESS_SECRET}
REFRESH_SECRET= {YOUR_JWT_REFRESH_SECRET}

AUTH_GMAIL_FROM = {YOUR_GMAIL_ACCOUNT_NAME}
AUTH_GMAIL_PASSWORD = {YOUR_GMAIL_ACCESS_TOKEN}
```
