🌲 코드숲 (CodeSoop)

개발자들이 질문하고, 답하고, 대화하며 성장하는
게시판 기반 개발자 커뮤니티 웹 서비스

📌 프로젝트 소개

코드숲은 단순 Q&A 게시판을 넘어
게시글·댓글·실시간 채팅을 통해
개발자 간의 지식 공유와 소통을 강화하기 위해 제작된 커뮤니티 서비스입니다.

게시판 중심 커뮤니티

권한 기반 사용자 / 관리자 기능

WebSocket을 활용한 1:1 실시간 채팅

🎯 기획 배경

기존 개발자 커뮤니티는 다음과 같은 한계를 가지고 있었습니다.

질문 이후 추가 소통이 어렵다

관리자 기능이 제한적이다

실시간 커뮤니케이션이 부족하다

👉 코드숲은
게시판 + 댓글 + 실시간 채팅을 결합하여
“질문 → 토론 → 대화”로 이어지는 구조를 목표로 합니다.

👤 타겟 사용자

코딩 입문자

주니어 개발자

개발 관련 질문 및 정보 공유를 원하는 사용자

✨ 주요 기능
사용자 기능

회원가입 / 로그인

게시글 작성 · 수정 · 삭제

댓글 작성 · 수정 · 삭제

작성자 클릭 시 1:1 채팅

마이페이지 (내 게시글 조회)

관리자 기능

전체 유저 조회

유저 차단 / 차단 해제

카테고리 관리 (대분류 / 소분류)

모든 게시글 / 댓글 관리

실시간 채팅

WebSocket + STOMP 기반

1:1 채팅

실시간 메시지 송수신

인증 사용자만 연결 가능

🏗 시스템 아키텍처
[ Client (React) ]
        ↓
[ Spring Boot API Server ]
        ↓
[ MySQL Database ]

[ WebSocket (STOMP) ]


REST API: 게시판 / 유저 / 관리자 기능

WebSocket: 실시간 채팅 처리

🛠 기술 스택
Backend

Java 21

Spring Boot

Spring Security

Spring Data JPA

WebSocket / STOMP

Frontend

React

Vite

TypeScript

Database

MySQL

Infra / Tool

Docker

Git / GitHub

IntelliJ IDEA

🔐 인증 / 인가

JWT 기반 인증

Access Token

Refresh Token

Spring Security 기반 권한 관리

ROLE_USER

ROLE_ADMIN

💬 채팅 기능 구조

WebSocket 연결

STOMP 프로토콜 사용

인증 토큰 기반 연결 검증

1:1 채팅방 생성 및 메시지 브로드캐스트

🚀 실행 방법
Backend 실행
./gradlew bootRun

Frontend 실행
npm install
npm run dev

🧪 주요 구현 포인트

REST API와 WebSocket의 역할 분리

권한(Role) 기반 기능 제어

관리자 기능과 일반 사용자 기능 분리

채팅 기능을 기존 게시판 서비스와 자연스럽게 연동
