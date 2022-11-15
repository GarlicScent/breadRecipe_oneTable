# 🥪Onetable

### 제빵 레시피 공유 사이트 제작

상세 소개: 코딩온 교육기관을 통해 진행한 세번째 프로젝트입니다. 요리 레시피 중 빵과 관련된 레시피를 공유하는 사이트를 제작하였으며, 2명씩 프론트와 백엔드로 역할을 나누어 4명이 한 조로 2주간 개발을 진행하였습니다.

## :link: Link
[Onetable](http://3.37.87.185:8002/)

## :date: 기간

2022.09.19 ~ 2022.10.04

## ERM
<img src="https://user-images.githubusercontent.com/26360179/196043616-ac2ee3b7-500b-40cf-be25-4c3dcf0ac424.png" width="600"/>
<hr />

## 💁🏻 개발 내용
### 메인 & 유저 페이지

- sequelize `.findAll()`로 레시피 데이터 추출
    - main page
        - `group by`로 하여 묶은 그룹의 `count` 높은 순으로 추출
        - `include`를 통해 Recipe 테이블을 left join하여 레시피 검색
        - `limit: 10` 으로 최대 10개만 검색.
    - my page
        - 로그인된 유저의 아이디로 작성된 레시피 데이터 추출 (유저가 작성한 레시피 확인)
        - `include`를 통해 favorite에 recipe 테이블 left join (좋아요한 레시피 확인)

### 레시피 페이지

- sequelize 문법을 사용하여 등록 및 삭제 구현
    - `.create()` 레시피 등록
    - `.destroy()` 레시피 삭제
    
- 레시피 정렬
    - `group by`로 하여 묶은 그룹의 `count` 높은 순으로 추출
    - 카테고리 선택시 필터링하여 레시피 데이터 추출
- 레시피 좋아요 및 취소 기능
    - sequelize `.create()`로 좋아요 생성
    - sequelize `.destroy()`로 좋아요 취소
- 특정 레시피에서의 댓글 기능
    - sequelize `.create()`로 리뷰 등록
&nbsp;
## :movie_camera: 시연영상
![mainVidGif](https://user-images.githubusercontent.com/26360179/201862860-f34450d1-5950-4ba8-b4ca-2e304afe61b6.gif)


