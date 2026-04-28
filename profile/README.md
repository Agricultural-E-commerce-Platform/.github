# 🌾 Agricultural E-commerce Platform

> 동시성 제어와 성능 최적화를 중심으로 설계된  
> 농산물 특가 판매 이커머스 백엔드 프로젝트

---

## 🎯 프로젝트 소개

신선한 농산물을 온라인으로 구매할 수 있는 이커머스 플랫폼입니다.  
일반 상품과 한정 수량 타임세일 상품을 함께 제공하며,  
동시성 문제와 성능 이슈를 실제 서비스 수준으로 해결하는 것을 목표로 합니다.

---

## 🧩 핵심 구현 포인트

### 1️⃣ 쿠폰 동시성 제어

- Redis 분산 락 기반 선착순 쿠폰 발급
- DB 조건부 UPDATE로 초과 발급 방지
- Fail Fast 전략 적용

---

### 2️⃣ 재고 차감 정합성

- Redis 락 + DB 조건 검증 (이중 방어)
- 재고 음수 방지
- Deadlock 방지 (락 순서 정렬)

---

### 3️⃣ 검색 성능 개선

- 검색 API v1 / v2 분리
- Caffeine Cache 적용
- Redis Sorted Set 기반 인기 검색어 실시간 집계

---

## 🏗️ 아키텍처

> 전체 시스템 구조

<img width="3324" height="2684" alt="서버 아키텍쳐 구조도" src="https://github.com/user-attachments/assets/7c5ae5f3-b16d-4ab7-80f8-5ed236936fa2" />


---

## 🔗 Repository

| 구분 | 링크 |
|------|------|
| 📦 Code | https://github.com/Agricultural-E-commerce-Platform/Agricultural-E-commerce-Platform.git |
| 📄 Docs | https://github.com/Agricultural-E-commerce-Platform/Agricultural-E-commerce-Platform-Docs.git |

---

## 📅 프로젝트 기간

2026.04.08 ~ 2026.04.28

[마일스톤](https://github.com/Agricultural-E-commerce-Platform/Agricultural-E-commerce-Platform-Docs/blob/50c7d199a2d3525c6ee79ca0020525c3b0881502/documents/milestone/Milestone.md)

---

## 👥 팀원

| 이름 | 역할 | GitHub | Blog |
|------|------|--------|------|
| 정지훈 | 팀장 / DevOps | https://github.com/doksakim7 | https://velog.io/@jhsky3118/posts |
| 정은지 | 부팀장 | https://github.com/eunjiom/ | https://eunjiom.tistory.com/ |
| 김예은 | QA / 서기 | https://github.com/rioloe | https://velog.io/@rioluz |
| 이중현 | QA 총괄 / DB | https://github.com/RootToApex | https://velog.io/@dlwndgus012/posts |

---

## ⚙️ 기술 스택

### Backend
- Java 17, Spring Boot 3.x
- Spring Security + JWT
- Spring Data JPA, QueryDSL

### Infrastructure
- MySQL, Redis
- Docker, Nginx
- GitHub Actions (CI/CD)

### Performance
- Redis Distributed Lock
- Caffeine Cache

---

# ⚖️ License
This documentation follows the MIT License of the main project.

See the LICENSE file in the main repository for details:  
https://github.com/Agricultural-E-commerce-Platform/Agricultural-E-commerce-Platform/blob/main/LICENSE
