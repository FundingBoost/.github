# FundingBoost(카카오톡 선물하기 기반 크라우드 펀딩 시스템)
##### 구태형, 맹인호, 임창희, 양혜인, 이재현, 이재현

## 1. 프로젝트 기획/배경

생일이나 기념일에 여러 개의 똑같은 저가의 상품 대신 평소에 받고 싶었던 고가의 상품을 펀딩을 통해 구매하자!

### 기대 효과
- 친구에게 고민없이 만족을 줄 수 있는 맞춤형 선물을 줄 수 있다.
- 상품 금액에 구애받지 않고 원하는 금액만큼 자유롭게 선물 할 수 있고, 큰 금액의 선물도 별다른 정산 과정 없이 간편하게 선물 할 수 있다.

## 2. 프로젝트 일정
<img width="800" alt="image" src="https://github.com/user-attachments/assets/36cff3bc-2264-4a28-966b-e41ec7491881">

**1. 프로젝트 기획 및 설계**
  - 아이디어 도출 및 기획
  - 여러 산출물 작성 및 아이디어 구체화
  - 팀내 규율 및 Convention 정의

**2. 펀딩 서비스 구현 및 배포**
  - 펀딩에 관련된 서비스 구현
  - 크램폴린으로 배포 후 V1 로직 테스트

**3. 로그인 및 쇼핑 서비스 구현 및 배포**
  - 쇼핑에 관련된 서비스 구현
  - JWT를 이용한 로그인 구현
  - 배포 환경에서 Redis 추가 배포

**4. 소셜 로그인 및 검색 구현 및 배포**
  - 카카오톡 OAuth 구현
  - 검색 기능 구현
  - Promethus & Grafana 추가 배포

## 3. 서비스 산출물

<img width="621" alt="image" src="https://github.com/user-attachments/assets/584b3c1e-34e2-4753-97c6-224a21051fab">
<img width="621" alt="image" src="https://github.com/user-attachments/assets/d7e1d980-c543-4954-aea5-126a0efbd504">

## 4. Tech Stack

- Front-end : React, Scss, Recoil, npm, axios, React Bootstrap
- Back-end : Spring Boot, Spring Data JPA, Spring Security, JWT, Gradle, Tomcat, Postman, Swagger, Junit, mockito, OAuth
- Infra : Krampoline, Docker, Nginx, KargoCD
- DataBase : H2, MariaDB, Redis
- Collaboration Tools : Github, Kakao Talk, ERD Cloud, Jira, Confluence, Google Drive, Figma
- Monitoring : Prometheus, Grafana
- IDE : Intellij, Web Storm, DataGrip

## 5. 기능 구현

### Front-end
1. **Atomic design pattern** : Component 개발

<img width="672" alt="image" src="https://github.com/user-attachments/assets/fcfc614f-f53e-4789-9af5-eef7cba765e7">

- **페이지 단위 개발** : 재사용이 가능한 컴포넌트를 만들어 조립하는 방식의 개발
- **작업물의 전체적인 컨셉과 분위기 통일감 부여(톤앤매너)**

2. **코드스플리팅** : 페이징 로딩 속도 개선

<img width="613" alt="image" src="https://github.com/user-attachments/assets/e92293c0-9ae5-4eca-857a-d5a4ab96d544">

- 문제 : 용량 증가로 페이지 로딩 속도 개선
- **해결** : 페이지 로딩 속도 성능 증가

### Back-end
1. **사용자 편의성 고려**
  - OAuth를 이용한 **카카오톡 로그인**
  - 카카오톡 서버에서 **친구 목록 가져오기 API**를 통해 친구 목록 조회 가능

3. **동시성 문제 관리**
<img width="658" alt="image" src="https://github.com/user-attachments/assets/6c6d66a4-0c7b-40e3-9f9e-fd55e24057d3">

4. **성능 개선** : 쇼핑 페이지 조회 및 검색<br>
  - 상품 개수 : 18,743건

<img width="641" alt="image" src="https://github.com/user-attachments/assets/b0eeeb7a-1291-4bf4-9696-fcb8f7e2e296">


### 배포(Krampoline IDE)

<img width="561" alt="image" src="https://github.com/user-attachments/assets/a5dcd7a1-b1b5-4ddf-b2bb-05a1e70a4ed8">

#### Application 배포
- Client, Server 배포
- Client는 React, Server는 Spring Boot
- 요청에 대한 분산 처리

#### In memory DB
- 동시성 제어를 위한 Redis
- 로그인을 위한 Redis

#### 서버 모니터링
- 서버 리소스 모니터링
- 성능 테스트 모니터링

## 6. 협업

1. Jira, Confluence
- 이슈 관리
- 스크림 및 정기 회의 기록 관리

2. GitHub
- 코드 형상 관리
- [코드 | 커밋 | PR] 컨벤션 적용
- [배포 | 개발] 브랜치 전략

3. Kakao Talk, Slack
- 리소스 공유
- 회의 안건 공유

4. Figma
- 기획/디자인
- 서비스 아키텍처 구성
- UI 설계
  
## 7. Github
https://github.com/FundingBoost


## 8. Jira
https://kcsfinalproject.atlassian.net/jira/projects?selectedProjectType=software

## 9. Confluence
https://kcsfinalproject.atlassian.net/wiki/spaces/KAN/overview?homepageId=98536

## 10. 발표자료
[FundingBoost Final PPT_v3.pdf](https://github.com/user-attachments/files/16691153/FundingBoost.Final.PPT_v3.pdf)

## 11. 카카오 클라우드 스쿨 4기 수료영상
https://www.youtube.com/watch?v=-va9M4iUHuI
