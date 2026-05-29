---
title: "IaaS PaaS SaaS On-Prem"
categories:
  - infra/cloud
tags:
  - cheatsheet
  - cloud
  - iaas
  - paas
  - saas
  - on-prem
---

IaaS, PaaS, SaaS, On-Prem 차이


# IaaS PaaS SaaS On-Prem
## 특징 비교

```text
On-Prem  : 회사가 서버, 네트워크, 스토리지, OS, 런타임, 앱 전부 관리
IaaS     : 클라우드가 하드웨어 제공, 회사가 OS부터 앱까지 관리
PaaS     : 클라우드가 인프라와 런타임 제공, 회사가 코드와 데이터 중심 관리
SaaS     : 완성된 소프트웨어를 서비스로 사용, 회사는 설정과 사용자 관리 중심
```

- `On-Prem`
  - 직접 구축, 직접 운영
- `IaaS`
  - 가상 서버 임대
- `PaaS`
  - 배포 플랫폼 사용
- `SaaS`
  - 완성 제품 구독

## 예시

```text
사내 메일 서버 직접 설치, 서버실 운영               -> On-Prem
AWS EC2 에 애플리케이션 직접 배포                  -> IaaS
Google App Engine, Azure App Service 에 코드 배포 -> PaaS
Gmail, Slack, Notion 사용                          -> SaaS
```

## 관리 책임

```text
영역                 On-Prem   IaaS   PaaS   SaaS
-------------------------------------------------
네트워크/스토리지      회사      클라우드  클라우드  클라우드
서버 하드웨어          회사      클라우드  클라우드  클라우드
가상화 계층            회사      클라우드  클라우드  클라우드
OS                    회사      회사      클라우드  클라우드
미들웨어/런타임        회사      회사      클라우드  클라우드
애플리케이션           회사      회사      회사      클라우드
데이터/설정            회사      회사      회사      일부 회사
```

핵심:

- 왼쪽으로 갈수록 직접 제어 증가
- 오른쪽으로 갈수록 운영 부담 감소

## On-Prem

```text
예시
- 회사 서버실에 물리 서버 구매
- 방화벽, 스위치, 스토리지 직접 구성
- OS 설치, 패치, 백업, 모니터링 직접 운영
```

- 장점
  - 통제력 높음
  - 규제, 망분리, 특수 보안 요구 대응 쉬움
- 단점
  - 초기 비용 큼
  - 증설 느림
  - 운영 인력 필요

## IaaS

```text
예시
- AWS EC2
- Google Compute Engine
- Azure VM
```

```bash
ssh ubuntu@server
sudo apt update
sudo apt install nginx
git clone https://github.com/example/app.git
docker compose up -d
```

- 서버는 빌리지만 운영은 직접 많이 함
- OS, 패치, 런타임, 배포 구조 직접 챙겨야 함

## PaaS

```text
예시
- Heroku
- Google App Engine
- Azure App Service
- AWS Elastic Beanstalk
```

```bash
git push platform main
```

- 인프라보다 코드 배포에 집중
- 오토스케일, 로그, 배포 편의성 좋음
- 플랫폼 제약 존재 가능

## SaaS

```text
예시
- Google Workspace
- Slack
- GitHub
- Notion
```

```text
회사 작업
- 계정 생성
- 권한 설정
- 결제 관리
- 사용 정책 설정
```

- 가장 빠르게 도입 가능
- 커스터마이징 범위 제한
- 벤더 정책 영향 큼

## 언제 무엇을 선택하는가

```text
직접 통제, 특수 보안, 레거시 장비 연동 중요   -> On-Prem
서버 제어 필요, 클라우드 유연성 필요         -> IaaS
개발 속도, 배포 편의성, 운영 단순화 중요      -> PaaS
기능을 바로 써야 하고 직접 개발 불필요        -> SaaS
```

## 자주 같이 나오는 말

```text
Public Cloud  : AWS, GCP, Azure 같은 퍼블릭 클라우드 사용
Private Cloud : 특정 조직 전용 클라우드 환경
Hybrid Cloud  : On-Prem + Cloud 함께 사용
```

- `On-Prem` 과 `Private Cloud` 는 같지 않음
  - On-Prem 은 자체 구축 환경 의미가 강함
  - Private Cloud 는 전용 클라우드 운영 방식 의미가 강함

## 빠른 판단표

```text
질문                                         추천
--------------------------------------------------------
완성된 협업 도구 바로 쓰고 싶은가               SaaS
코드만 배포하고 서버 관리 줄이고 싶은가         PaaS
OS, 네트워크, 서버 설정 직접 만지고 싶은가      IaaS
물리 장비와 내부망 통제까지 직접 필요한가        On-Prem
```

## 모음집

- `On-Prem`
  - 직접 구매, 직접 운영
- `IaaS`
  - 인프라는 클라우드, OS부터 앱은 직접 관리
- `PaaS`
  - 플랫폼 위에 코드 배포 중심
- `SaaS`
  - 완성된 소프트웨어 구독 사용
- `Hybrid Cloud`
  - 온프레미스와 클라우드 혼합 운영