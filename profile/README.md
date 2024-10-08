# FundingBoost(카카오톡 선물하기 기반 크라우드 펀딩 시스템)

- 프로젝트 기간 : 2024.03.28 ~ 2024.06.11
- 프로젝트 구성원
  - **Front-end**: [양혜인](https://github.com/happynow7), [현세미](https://github.com/SemiHyeon)
  - **Back-end**: [구태형](https://github.com/koosco), [맹인호](https://github.com/MeangSung), [임창희](https://github.com/ChangHee98), [이재현](https://github.com/JHyun0302)
 
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

| <div style="text-align: center;"> Front-end <br> <img width="175" alt="image" src="https://github.com/user-attachments/assets/1e8b029c-1d52-45e0-86c5-dce110b17cf4"> </div> | <div style="text-align: center;"> Back-end <br> <img width="225" alt="image" src="https://github.com/user-attachments/assets/56c8ddc7-fb39-48cd-9759-c4e9e74da418"> </div> |
|:---------------------------------------------------------------------------------------------------------------------------------------:|:------------------------------------------------------------------------------------------------------------------------------:|
| <div style="text-align: center;"> Infra <br> <img width="190" alt="image" src="https://github.com/user-attachments/assets/14b5ad40-dceb-4504-9d94-407edbb05589"> </div> | <div style="text-align: center;"> Collaboration Tools <br> <img width="181" alt="image" src="https://github.com/user-attachments/assets/e720a42f-8464-4aff-b9c6-0a9c5900dcad"> </div> |
| <div style="text-align: center;"> DataBase <br> <img width="181" alt="image" src="https://github.com/user-attachments/assets/08f77b4c-11f7-4847-93b6-e76a5031fb59"> </div> | <div style="text-align: center;"> Monitoring <br> <img width="112" alt="image" src="https://github.com/user-attachments/assets/058e1b84-fbab-468b-b004-a49ba1446be2"> </div> |
| <div style="text-align: center;"> IDE <br> <img width="108" alt="image" src="https://github.com/user-attachments/assets/47ad650d-416f-4519-a738-3670d32f67e4"> </div> | |

## 5. 주요 기능

| <div style="text-align: center;"> My 펀딩 생성 과정 <br> <img width="416" alt="image" src="https://github.com/user-attachments/assets/d75e4f15-c804-4b8e-aeba-0fc60844fef0"> </div> | <div style="text-align: center;"> 친구 펀딩 참여 과정 <br> <img width="416" alt="image" src="https://github.com/user-attachments/assets/145935cc-aaff-47f8-931e-2f1ce8928fbb"> </div> |
|:------------------------------------------------------------------------------------------------------------------------------------------------:|:-------------------------------------------------------------------------------------------------------------------------------------------------:|
| <div style="text-align: center;"> 홈 화면 <br> <img width="259" alt="image" src="https://github.com/user-attachments/assets/3fb84ed4-7deb-4b42-878b-5d4b784806b0"> </div> | <div style="text-align: center;"> 마이 페이지 <br> <img width="258" alt="image" src="https://github.com/user-attachments/assets/24fa83cc-2e00-4490-91de-3627e38ac907"> </div> |

## 6. 기능 구현

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

## 7. 협업

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
  
## 8. Github
https://github.com/FundingBoost

## 9. Jira
https://kcsfinalproject.atlassian.net/jira/projects?selectedProjectType=software

## 10. Confluence
https://kcsfinalproject.atlassian.net/wiki/spaces/KAN/overview?homepageId=98536

## 11. 발표자료
[FundingBoost Final PPT_v3.pdf](https://github.com/user-attachments/files/16691153/FundingBoost.Final.PPT_v3.pdf)

## 12. 카카오 클라우드 스쿨 4기 수료영상
https://www.youtube.com/watch?v=-va9M4iUHuI
