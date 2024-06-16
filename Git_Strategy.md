# Git Strategy

### 1. Git 브랜치 전략

#### 1.1 Git Flow

Git Flow는 기능 개발, 릴리스 준비, 유지보수 등을 체계적으로 관리하기 위한 브랜칭 모델입니다.

**브랜치 종류:**
- `main` 또는 `master`: 배포 가능한 안정된 코드
- `develop`: 개발 중인 코드, 다음 릴리즈 후보
- `feature/*`: 새로운 기능 개발 브랜치
- `release/*`: 릴리스 준비 브랜치
- `hotfix/*`: 긴급 버그 수정 브랜치
- `bugfix/*`: 일반 버그 수정 브랜치

**워크플로우:**
1. `main`에서 `develop` 브랜치 생성
2. 기능 개발은 `feature` 브랜치에서 수행 (`feature/feature-name`)
3. 기능 개발 완료 후 `develop` 브랜치로 병합
4. 릴리스 준비 시 `release` 브랜치 생성, 최종 테스트 및 수정
5. 릴리스 완료 후 `release` 브랜치를 `main`과 `develop`에 병합
6. 긴급 수정은 `hotfix` 브랜치에서 수행 후 `main`과 `develop`에 병합

**예시:**
```bash
# feature 브랜치 생성 및 작업
git checkout -b feature/login

# 작업 후 develop에 병합
git checkout develop
git merge feature/login

# 릴리스 준비
git checkout -b release/1.0.0

# 릴리스 후 main과 develop에 병합
git checkout main
git merge release/1.0.0
git checkout develop
git merge release/1.0.0
```

#### 1.2 GitHub Flow

GitHub Flow는 단순한 브랜칭 모델로, 항상 최신 상태를 유지하고 작은 배포를 자주 하는 것을 목표로 합니다.

**브랜치 종류:**
- `main`: 배포 가능한 안정된 코드
- 기능 브랜치: 단일 목적의 짧은 수명의 브랜치 (예: `feature/short-description`)

**워크플로우:**
1. `main`에서 기능 브랜치 생성
2. 기능 개발 완료 후 Pull Request 생성
3. 코드 리뷰 및 테스트 후 `main`에 병합
4. `main` 브랜치에서 배포

**예시:**
```bash
# 기능 브랜치 생성 및 작업
git checkout -b feature/login

# 작업 후 main에 병합 요청
git checkout main
git merge feature/login
```

#### 1.3 GitLab Flow

GitLab Flow는 GitHub Flow와 Git Flow의 장점을 결합한 모델로, 환경별 브랜치 전략을 추가로 도입합니다.

**브랜치 종류:**
- `main` 또는 `master`: 배포 가능한 안정된 코드
- `develop`: 개발 중인 코드
- 기능 브랜치: 기능 개발을 위한 브랜치 (예: `feature/short-description`)
- 환경 브랜치: 각 배포 환경을 위한 브랜치 (예: `staging`, `production`)

**워크플로우:**
1. `develop`에서 기능 브랜치 생성
2. 기능 개발 완료 후 `develop`에 병합
3. `develop`에서 환경 브랜치로 병합 (예: `staging`)
4. 환경 브랜치에서 최종 테스트 후 `main`에 병합

**예시:**
```bash
# 기능 브랜치 생성 및 작업
git checkout -b feature/login

# 작업 후 develop에 병합
git checkout develop
git merge feature/login

# 환경 브랜치로 병합 (staging)
git checkout staging
git merge develop

# 최종 테스트 후 main에 병합
git checkout main
git merge staging
```

### 2. 커밋 메시지 전략

**규칙:**
1. **제목 (subject)**: 50자 이내, 대문자로 시작, 마침표 금지
2. **본문 (body)**: 72자 이내 줄, 한 줄 비워두고 작성, 변경 이유와 주요 변경 사항 설명
3. **푸터 (footer)**: 관련 이슈 번호나 참고 정보

**타입:**
- `feat`: 새로운 기능
- `fix`: 버그 수정
- `docs`: 문서 수정
- `style`: 코드 포맷팅
- `refactor`: 코드 리팩토링
- `test`: 테스트 추가
- `chore`: 기타 변경 사항

**예시:**
```plaintext
feat(auth): add JWT authentication

Implemented JSON Web Token (JWT) authentication to enhance security.
Users can now log in using their credentials and receive a token for
subsequent requests. This update also includes unit tests for the
authentication module.

Resolves: #456
```

### 3. 코드 리뷰 및 병합 전략

**코드 리뷰:**
- 모든 Pull Request는 적어도 한 명 이상의 리뷰어가 리뷰
- 코드 리뷰 시 피드백 제공 및 토론
- 주요 기능 변경 시 팀 전체 논의

**병합 전략:**
- **Squash and Merge**: 커밋 히스토리를 하나로 합쳐 깔끔하게 유지
- **Rebase and Merge**: 커밋 히스토리를 재배열하여 깔끔하게 유지, 충돌 해결 필요
- **Merge Commit**: 모든 커밋을 유지하며 병합, 히스토리가 복잡해질 수 있음

**예시:**
```bash
# 기능 브랜치에서 작업 후
git checkout develop
git merge --squash feature/login
```



