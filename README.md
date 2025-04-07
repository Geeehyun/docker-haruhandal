# docker-setup-haruhandal
하루한달 도커 설정파일 

# 🐳 Docker 기반 로컬 개발환경 세팅 가이드

이 저장소는 React + Spring Boot + MariaDB + Redis 기반의 로컬 개발환경을 Docker로 구성한 세팅입니다.  
`docker-compose` 명령어 한 줄로 모든 서비스를 실행할 수 있어요!

---

## 📦 구성 서비스

| 이름        | 포트     | 설명                         |
|-------------|----------|------------------------------|
| React Front | 3000     | 프론트엔드(Vue/React 등)     |
| Spring Boot | 8080     | 백엔드 API 서버              |
| MariaDB     | 3306     | 관계형 데이터베이스          |
| Redis       | 6379     | 캐시 및 세션 저장소          |

---

## 🚀 시작 방법

1. Docker, Docker Desktop 설치  
   👉 https://www.docker.com/products/docker-desktop

2. GitHub에서 이 프로젝트 클론
   
```bash
git clone https://github.com/your-org/project-docker-setup.git
cd project-docker-setup
```

3. 백엔드 jar 파일 빌드
(필요 시)

```bash
cd backend/your-backend-dir
./gradlew build
```

4. 전체 서비스 실행

```bash
docker compose up --build
```

5. 서비스 접속
- 프론트엔드: http://localhost:3000
- 백엔드 API: http://localhost:8080

## 📁 폴더 구조
```
.
├── backend/api-haruhandal
│   ├── Dockerfile
│   └── backend 소스파일들...
├── frontend/front-haruhandal
│   ├── Dockerfile
│   └── frontend 소스파일들...
├── docker-compose.yml
└── README.md
```

## 🙋‍♀️ 개발 흐름 (참고)
1. 인텔리제이로 코드 수정
2. frontend는 실시간 반영
3. backend는 ./gradlew build 후 재시작 필요


