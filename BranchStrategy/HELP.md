## 🤙🏻 Git Branch & Commit Convention

---

### 📌 Branch Strategy

#### 🌳 Main Branches

| 브랜치    | 설명                                           |
|--------|----------------------------------------------|
| `main` | 실제 서비스에 배포되는 운영 브랜치                          |
| `dev`  | 기능 브랜치들이 병합되는 통합 개발 브랜치 (테스트 완료 후 main으로 병합) |

#### 🌿 Feature Branches

- 브랜치는 아래 prefix를 사용해 목적을 명확히 구분합니다:
    - `feat/기능명`: 기능 개발
    - `fix/버그명`: 버그 수정
    - `refactor/모듈명`: 리팩토링 (동작 변경 없음)
    - `docs/문서명`: 문서 수정
    - `test/모듈명`: 테스트 코드 추가
    - `hotfix/패치명`: 긴급 패치 (운영 중 버그 등)
    - `release/버전명`: 배포 버전 준비

> 예: `feat/login-api`, `fix/user-auth-token`, `refactor/controller-structure`

---

### 📌 Branch Naming Convention

> **이슈번호/브랜치타입/기능명**  
> 예: `123/feat/login-api`, `57/fix/image-preview`

- 이슈번호를 붙이면 GitHub, Jira 등과 연동 시 자동 링크 가능

---

### 📌 Commit Convention

#### 🧱 커밋 메시지 구조

```plaintext
<타입>: <제목>  // 제목은 최대 50자 이내, 마침표 금지

본문 내용 (선택)  
- 무엇을, 왜 했는지 설명  
- 필요한 경우 이슈 번호 참조 (#123)

BREAKING CHANGE: (선택, 하위 호환 불가 변경 사항 설명)