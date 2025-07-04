# UFC Community Project

UFC 팬들을 위한 커뮤니티 웹 애플리케이션입니다. Spring Boot와 Next.js를 기반으로 한 풀스택 프로젝트입니다.

## 🌟 주요 기능

- 사용자 인증 (JWT, 소셜 로그인)
- 게시글 작성, 조회, 수정, 삭제
- 댓글 기능
- 선수 정보 및 경기 결과 조회

## 🛠️ 기술 스택

### Backend

- **Framework**: Spring Boot 3.5.3
- **Language**: Java 17
- **Build Tool**: Gradle
- **Dependencies**:
  - Spring Web, Spring Data JPA, Spring Security, OAuth2 Client
  - JWT (JSON Web Token)
  - MySQL, Redis
  - Lombok
  - Springdoc OpenAPI (Swagger)

### Frontend

- **Framework**: Next.js 15.3.5 (with Turbopack)
- **Language**: TypeScript
- **Styling**: Tailwind CSS
- **Dependencies**:
  - React, React DOM
  - Axios (for API communication)
  - React Query (for server state management)
  - Zustand (for client state management)
  - React Hook Form
  - NextAuth.js

### DevOps & Database

- **Containerization**: Docker, Docker Compose
- **Database**: MySQL 8.0, Redis 7
- **Web Server**: Embedded Tomcat (in Spring Boot)

## 📂 프로젝트 구조

```
ufc-community/
├── backend/      # Spring Boot 백엔드 서버
├── frontend/     # Next.js 프론트엔드 애플리케이션
├── docker-compose.yml # Docker 서비스 정의
└── Readme.md
```

## 🚀 실행 방법

### Prerequisites

- [Docker](https://www.docker.com/get-started)
- [Docker Compose](https://docs.docker.com/compose/install/)

### Installation & Running

1.  프로젝트를 클론합니다.
    ```bash
    git clone https://github.com/your-username/ufc-community.git
    cd ufc-community
    ```

2.  Docker Compose를 사용하여 모든 서비스를 실행합니다.
    ```bash
    docker-compose up -d --build
    ```

3.  애플리케이션 접속
    - **Frontend**: [http://localhost:3000](http://localhost:3000)
    - **Backend API (Swagger UI)**: [http://localhost:8080/swagger-ui.html](http://localhost:8080/swagger-ui.html)

## 🐳 Docker 서비스 정보

- **`ufc-mysql`**: MySQL 데이터베이스. 포트 `3306`으로 노출됩니다.
- **`ufc-redis`**: Redis 서버. 포트 `6379`로 노출됩니다.
- **`ufc-backend`**: Spring Boot 애플리케이션. 포트 `8080`으로 노출됩니다.
- **`ufc-frontend`**: Next.js 애플리케이션. 포트 `3000`으로 노출됩니다.
