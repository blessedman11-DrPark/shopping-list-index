# 쇼핑 리스트 - Dr.Park

Supabase 데이터베이스와 연동된 쇼핑 리스트 웹 애플리케이션입니다.

## 배포 URL

**https://shopping-list-drpark.vercel.app**

## 연동 서비스

| 서비스 | 프로젝트명 | 용도 |
|--------|-----------|------|
| **Vercel** | shopping-list-drpark | 웹 호스팅 & 자동 배포 |
| **GitHub** | shopping-list-drpark | 소스 코드 관리 |
| **Supabase** | shopping-list-drpark | PostgreSQL 데이터베이스 |

## 자동 배포 플로우

```
GitHub (main 브랜치) push → Vercel 자동 감지 → 프로덕션 배포
```

## 주요 기능

### 1. 아이템 추가
- 입력창에 아이템 이름 입력
- **추가** 버튼 클릭 또는 **Enter** 키로 추가
- Supabase 데이터베이스에 자동 저장

### 2. 아이템 체크/해제
- 아이템 왼쪽의 **원형 체크박스** 클릭
- 체크된 아이템은 취소선 표시
- 완료 개수 자동 집계

### 3. 아이템 이름 수정
- 아이템 **텍스트 클릭** → 수정 모드 진입
- 새 이름 입력 후:
  - **Enter** → 저장
  - **Escape** → 취소
  - **외부 클릭** → 저장

### 4. 아이템 삭제
- 아이템 오른쪽의 **× 버튼** 클릭
- 즉시 삭제 (확인 없음)

## 기술 스택

- **Frontend**: HTML, CSS, JavaScript (Vanilla)
- **Backend**: Supabase (PostgreSQL)
- **Hosting**: Vercel
- **Version Control**: GitHub

## 데이터베이스 구조

**테이블: shopping_items**

| 컬럼 | 타입 | 설명 |
|------|------|------|
| id | UUID | 기본키 (자동 생성) |
| text | TEXT | 아이템 이름 |
| checked | BOOLEAN | 체크 여부 |
| created_at | TIMESTAMP | 생성 시간 |

## 버전 히스토리

| 버전 | 날짜 | 내용 |
|------|------|------|
| v1.0-backup | 2026-01-29 | 아이템 수정 기능 추가 완료 |

---

Made with Claude Code
