---
title: "Terminal Command"
categories:
  - tools/terminal
tags:
  - cheatsheet
  - terminal
  - command
  - windows
  - path
---

개발할 때 자주 쓰는 터미널 명령어 모음


# Terminal Command
## 현재 위치, 파일 목록 확인

```bash
pwd
ls
ls -la
```

Windows CMD

```bash
cd
dir
```

- `pwd`
  - 현재 작업 경로 확인
- `ls`
  - 현재 폴더 파일 목록 확인
- `ls -la`
  - 숨김 파일 포함 전체 목록 확인
- `cd`
  - Windows CMD에서 현재 경로 확인
- `dir`
  - Windows CMD에서 파일 목록 확인

## 폴더 이동

```bash
cd project
cd ..
cd /
cd D:\project\hdchoi-dev.github.io
```

- `cd project`
  - 현재 폴더 안 `project` 로 이동
- `cd ..`
  - 상위 폴더로 이동
- `cd /`
  - 루트 경로로 이동

## 상대 경로

현재 위치 기준 경로

예시:

```bash
_posts/2026-05-25-terminal-command.md
./_posts/2026-05-25-terminal-command.md
../images/logo.png
```

- `_posts/...`
  - 현재 폴더 안 `_posts` 기준 이동
- `./`
  - 현재 폴더 의미
- `../`
  - 상위 폴더 의미


## 파일, 폴더 생성

```bash
touch memo.txt
mkdir src
mkdir images
```

Windows CMD

```bash
echo. > memo.txt
mkdir src
```

- `touch memo.txt`
  - 빈 파일 생성
- `mkdir src`
  - 새 폴더 생성

## 파일 복사, 이동, 삭제

```bash
cp app.js app.backup.js
mv old.txt new.txt
rm memo.txt
rm -r temp
```

Windows CMD

```bash
copy app.js app.backup.js
move old.txt new.txt
del memo.txt
rmdir /s temp
```

> `rm -r`, `rmdir /s` 는 복구 어려움. 경로 확인 후 실행.

## 파일 내용 확인

```bash
cat README.md
type README.md
```

- `cat README.md`
  - 파일 내용 출력
- `type README.md`
  - Windows CMD에서 파일 내용 출력

## 검색

```bash
find . -name "*.md"
grep -R "TODO" .
grep -R "title" _posts
```

Windows CMD 기준:

```bash
dir /s /b *.md
findstr /s /n /i "TODO" *.*
findstr /s /n /i "title" _posts\*.*
```

- `find . -name "*.md"`
  - markdown 파일 찾기
- `grep -R "TODO" .`
  - 현재 폴더 전체 문자열 검색
- `findstr /s /n /i "TODO" *.*`
  - Windows CMD에서 하위 폴더 포함 문자열 검색

## 개발할 때 자주 쓰는 명령

```bash
history
echo $PATH
code .
```

Windows CMD 기준:

```bash
tasklist
netstat -ano | findstr :3000
echo %PATH%
code .
```

- `tasklist`
  - 실행 중 프로세스 목록 확인
- `netstat -ano | findstr :3000`
  - 3000 포트 사용 프로세스 확인
- `code .`
  - 현재 폴더를 VS Code로 열기

## 자주 쓰는 조합

### 현재 위치와 파일 목록 같이 보기

```bash
pwd
ls -la
```

### markdown 파일 찾기

```bash
find . -name "*.md"
dir /s /b *.md
```

### TODO 문자열 전체 검색

```bash
grep -R "TODO" .
findstr /s /n /i "TODO" *.*
```

### 특정 포트 점유 프로세스 찾기

```bash
netstat -ano | findstr :8080
tasklist | findstr 1234
```

## 모음집

- `pwd`
  - 현재 작업 경로 확인
- `ls`
  - 파일 목록 확인
- `cd ..`
  - 상위 폴더 이동
- `mkdir 폴더명`
  - 폴더 생성
- `touch 파일명`
  - 빈 파일 생성
- `cat 파일명`
  - 파일 내용 확인
- `cp 원본 대상`
  - 파일 복사
- `mv 원본 대상`
  - 파일 이동 또는 이름 변경
- `rm 파일명`
  - 파일 삭제
- `find . -name "*.md"`
  - 특정 확장자 파일 검색
- `grep -R "문자열" .`
  - 현재 폴더 전체 문자열 검색
- `dir`
  - Windows CMD에서 파일 목록 확인
- `type 파일명`
  - Windows CMD에서 파일 내용 확인
- `copy 원본 대상`
  - Windows CMD에서 파일 복사
- `move 원본 대상`
  - Windows CMD에서 파일 이동
- `del 파일명`
  - Windows CMD에서 파일 삭제
- `findstr /s /n /i "문자열" *.*`
  - Windows CMD에서 문자열 검색