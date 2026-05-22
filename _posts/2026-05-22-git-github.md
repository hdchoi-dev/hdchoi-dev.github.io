---
title: "Git/GitHub"
categories:
  - Cheatsheet
tags:
  - git
  - github
  - command
---

# Git
## 로컬 프로젝트 GitHub 원격 저장소 연동

```bash
git init
git remote add origin https://github.com/USERNAME/REPOSITORY.git
git branch -M main
git pull origin main
git status
git add .
git add src/app.js README.md
git commit -m "작업 내용 요약"
git push
```

## 원격 레포 최신 변경 pull

git pull origin main

## 브랜치

```bash
git checkout -b feature/login
git checkout main
```
checkout main > main으로 전환


## 커밋 수정

### 마지막 커밋 메시지 수정

```bash
git commit --amend -m "새 커밋 메시지"
```

### 마지막 커밋에 파일 추가

```bash
git add .
git commit --amend
```

이미 원격에 push 했으면 강제 push

```bash
git push --force-with-lease
```

## 추적되지 않은 파일, 변경 파일 확인

```bash
git status
git diff
git diff --staged
```

- `git diff`: 아직 add 안 한 변경 보기
- `git diff --staged`: add 한 변경 보기

## 작업 되돌리기

### add 전 수정 내용 되돌리기

```bash
git restore 파일명
```

### add 한 상태 취소

```bash
git restore --staged 파일명
```

### 마지막 커밋만 취소하고 변경 내용은 남기기

```bash
git reset --soft HEAD~1
```

### 마지막 커밋과 변경 내용 모두 취소

```bash
git reset --hard HEAD~1
```

> `reset --hard` 는 복구 어려움. 주의.

## 원격 브랜치 삭제

```bash
git branch -d feature/login
git push origin --delete feature/login
```
## 모음집

- `git remote -v`
  - 연결된 원격 저장소 주소 확인
- `git branch`
  - 로컬 브랜치 확인
- `git branch -a`
  - 원격 브랜치 확인
- `git init`
  - 현재 폴더를 Git 저장소로 초기화
- `git remote add origin <URL>`
  - 원격 저장소 등록
- `git branch -M main`
  - 기본 브랜치를 `main`으로 변경
- `git pull origin main`
  - 원격 `main` 최신 내용 가져오기
- `git add .`
  - 변경 파일 스테이징
- `git commit -m "메시지"`
  - 스테이징된 변경 커밋
- `git push -u origin main`
  - 원격 `main`으로 첫 업로드 + 추적 설정
- `git push`
  - 현재 브랜치 변경 원격 업로드
- `git checkout -b 브랜치명`
  - 새 브랜치 생성 후 이동
- `git switch -c 브랜치명`
  - 새 브랜치 생성 후 이동. 최신 문법
- `git switch main`
  - `main` 브랜치로 이동
- `git merge main`
  - 현재 브랜치에 `main` 변경사항 병합
- `git status`
  - 변경 상태 확인
- `git diff`
  - 작업 디렉토리 변경 확인
- `git diff --staged`
  - 스테이징된 변경 확인
- `git restore 파일명`
  - 수정 내용 되돌리기
- `git restore --staged 파일명`
  - 스테이징 취소
- `git reset --soft HEAD~1`
  - 마지막 커밋 취소, 변경은 유지
- `git reset --hard HEAD~1`
  - 마지막 커밋과 변경 모두 삭제
- `git branch -d 브랜치명`
  - 로컬 브랜치 삭제
- `git push origin --delete 브랜치명`
  - 원격 브랜치 삭제
- `git remote -v`
  - 원격 저장소 주소 확인

## Git commit 규칙 정리

목적: 커밋 메시지 일관성 유지.

기본 형식:

```text
type: subject
```

예시:

```text
feat: 로그인 API 추가
fix: 회원가입 유효성 검사 오류 수정
docs: README 설치 방법 보완
refactor: 게시글 정렬 로직 분리
chore: 의존성 버전 업데이트
style: 공백 및 들여쓰기 정리
test: user service 테스트 추가
```

### 자주 쓰는 type

- `feat`
  - 새 기능 추가
- `fix`
  - 버그 수정
- `docs`
  - 문서 수정
- `refactor`
  - 동작 변화 없는 구조 개선
- `style`
  - 포맷팅, 세미콜론, 공백 등 스타일 수정
- `test`
  - 테스트 추가 또는 수정
- `chore`
  - 빌드, 설정, 패키지 업데이트, 잡무성 변경

### 작성 규칙

- 한 줄 요약부터 작성
- type은 소문자 사용
- type 뒤에 콜론(`:`) 1개 사용
- subject는 짧고 바로 의미 전달
- 불필요한 감탄사, 장문 설명 제거
- 하나 커밋에는 하나 주제 유지

좋은 예:

```text
feat: 댓글 좋아요 기능 추가
fix: 잘못된 날짜 포맷 처리 수정
docs: 배포 절차 정리
```

나쁜 예:

```text
update
fix bug
여러 기능 한번에 수정
최종 수정본
```

### 추천 패턴

- 기능 추가
  - `feat: 게시글 검색 기능 추가`
- 버그 수정
  - `fix: 태그 필터 중복 적용 문제 수정`
- 리팩터링
  - `refactor: post service 응답 변환 로직 분리`
- 설정 변경
  - `chore: jekyll 설정값 정리`