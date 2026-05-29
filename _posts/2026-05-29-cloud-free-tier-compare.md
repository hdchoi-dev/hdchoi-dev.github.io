---
title: "Cloud Free Tier Compare"
categories:
  - infra/cloud
tags:
  - cheatsheet
  - cloud
  - aws
  - azure
  - gcp
  - oracle-cloud
  - ncp
  - free-tier
---

AWS, Azure, GCP, Oracle Cloud, NCP 무료 티어와 선택 기준 비교


# Cloud Free Tier Compare
## 한 번에 비교

```text
AWS           : 범용성 가장 큼, 무료는 크레딧 중심으로 보는 편이 안전
Azure         : 12개월 무료 + 항상 무료 같이 제공
GCP           : $300 크레딧 + e2-micro 항상 무료
Oracle Cloud  : Always Free VM 강점, 장기 테스트 서버 비교에 자주 등장
NCP           : 국내 서비스 연동 강점, 무료 티어보다 프로모션 확인 중요
```

## 빠른 선택

```text
실무 범용성, 레퍼런스      -> AWS
Microsoft 중심 회사        -> Azure
서버리스, 데이터, GKE      -> GCP
장기 무료 VM 테스트        -> Oracle Cloud
국내 서비스, 네이버 연동   -> NCP
```

## 무료 티어 비교

```text
AWS
- 새 고객 기준 최대 $200 크레딧
- Free plan 기준 약 6개월 체험 구조
- 항상 무료 서비스 30개+

Azure
- 신규 계정 12개월 무료 서비스 다수
- 항상 무료 서비스 65개+
- Linux/Windows VM 750시간 체험 가능

GCP
- 신규 계정 $300 크레딧
- 20개+ 항상 무료
- Compute Engine e2-micro 항상 무료

Oracle Cloud
- Always Free 중심
- AMD Micro VM 최대 2개 또는 Arm 자원 한도 기반 구성

NCP
- 상시 무료 티어보다 이벤트, 크레딧, 프로모션 확인 중요
```

## AWS

```text
예시
- EC2
- S3
- RDS
- EKS
```

- 서비스 수 많음
- 실무, 채용, 문서, 레퍼런스 강함
- 무료는 예전 `EC2 12개월 무료` 기억보다 현재 크레딧 구조로 확인하는 편이 안전

## Azure

```text
예시
- Azure VM
- Azure App Service
- Azure SQL
- AKS
```

- Microsoft 365, AD, .NET, SQL Server 연계 강함
- 12개월 무료 + 항상 무료 같이 제공
- 기업 환경, 하이브리드 운영에서 자주 선택

## GCP

```text
예시
- Compute Engine
- Cloud Run
- BigQuery
- GKE
```

- `$300` 크레딧 제공
- `e2-micro` 항상 무료 항목 존재
- 서버리스, 데이터, 쿠버네티스 경험 기준으로 자주 선택

## Oracle Cloud

```text
예시
- VM.Standard.E2.1.Micro
- Ampere A1
- Object Storage
```

- Always Free 체감 강함

## NCP

```text
예시
- Server
- Object Storage
- Load Balancer
- Cloud DB
```

- 국내 서비스, 한국어 문서, 로컬 지원 강점
- 네이버 서비스 연동 검토 시 자주 포함
- 무료 티어보다 가입 시점 프로모션 확인이 중요

## 체크 포인트

- `무료 티어` 와 `무료 크레딧` 은 다름
  - 무료 티어: 월 한도 기반
  - 무료 크레딧: 금액 소진 시 종료
- `Always Free` 라도 트래픽, 디스크, IP, 백업은 과금될 수 있음
- 가입 전 공식 페이지에서 다시 확인 필요