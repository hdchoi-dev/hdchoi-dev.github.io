---
title: "Edge Case: Nested and Mixed Lists"
categories:
  - Edge Case/test/test
tags:
  - content
  - css
  - edge case
  - lists
  - markup
---

Nested and mixed lists are an interesting beast. It's a corner case to make sure that

* Lists within lists do not break the ordered list numbering order
* Your list styles go deep enough.

### Ordered -- Unordered -- Ordered

1. ordered item
2. ordered item 
  * **unordered**
  * **unordered** 
    1. ordered item
    2. ordered item
3. ordered item
4. ordered item



### Ordered -- Unordered -- Unordered

1. ordered item
2. ordered item 
  * **unordered**
  * **unordered** 
    * unordered item
    * unordered item
3. ordered item
4. ordered item

### Unordered -- Ordered -- Unordered

* unordered item
* unordered item 
  1. ordered
  2. ordered 
    * unordered item
    * unordered item
* unordered item
* unordered item

### Unordered -- Unordered -- Ordered

* unordered item
* unordered item 
  * unordered
  * unordered 
    1. **ordered item**
    2. **ordered item**
* unordered item
* unordered item

### Task Lists

- [x] Finish my changes
- [ ] Push my commits to GitHub
- [ ] Open a pull request
  - [ ] Follow discussions
  - [x] Push new commits


- 사이드 프로젝트
  - 프로젝트A
  - 프로젝트B

- AI (또는 AI·LLM)

  - 에이전트
  - 프롬프트·RAG
  - 논문·서베이
  - 평가·관측

- 개발(= 개발 지식)

  - 언어·프레임워크
  - 아키텍처·설계
  - 테스트·품질
  - 인프라·DevOps
  - 데이터

- 도메인

  - SCM
  - PLM

- 일하는 방식

  - 프로세스·애자일
  - 커리어·조직문화
  - (선택) 생산성·툴
- 사이드 프로젝트

  - 프로젝트A
  - 프로젝트B

- AI (또는 AI·LLM)

  - 에이전트
  - 프롬프트·RAG
  - 논문·서베이
  - 평가·관측

- 개발(= 개발 지식)

  - 언어·프레임워크
  - 아키텍처·설계
  - 테스트·품질
  - 인프라·DevOps
  - 데이터

- 도메인

  - SCM
  - PLM

- 일하는 방식

  - 프로세스·애자일
  - 커리어·조직문화
  - (선택) 생산성·툴


- Projects / projects

  - Project A / project-a
  - Project B / project-b

- AI Engineering / ai

  - Agents / agents
  - Prompting & RAG / prompting-rag
  - Papers & Surveys / papers-surveys
  - Evaluation & Observability / evaluation-observability

- Software Engineering / engineering

  - Languages & Frameworks / languages-frameworks
  - Architecture & Design / architecture-design
  - Testing & Quality / testing-quality
  - Infrastructure & DevOps / infra-devops
  - Data Systems / data-systems

- Domain Knowledge / domain

  - SCM / scm
  - PLM / plm

- Work Practices / work

  - Process & Agile / process-agile
  - Career & Culture / career-culture
  - Productivity & Tools / productivity-tools
