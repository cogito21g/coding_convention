# Git Commit Message

### Commit Message 구조

Commit Message는 일반적으로 세 부분으로 나뉩니다:
1. **제목 (subject)**: 간결하고 명확한 변경 사항 요약
2. **본문 (body)**: (선택 사항) 변경 이유와 주요 변경 사항 설명
3. **푸터 (footer)**: (선택 사항) 관련된 이슈 번호나 참고 정보

#### 1. 제목 (subject)

- **형식**: `<타입>(<범위>): <변경 사항 요약>`
- **길이**: 50자 이내
- **내용**: 대문자로 시작하고 마침표 사용 금지

**예시:**
```
feat(user): add login functionality
```

#### 2. 본문 (body)

- **형식**: 한 줄 비워두고 작성
- **길이**: 한 줄당 72자 이내
- **내용**: 무엇을, 왜 변경했는지 설명

**예시:**
```
feat(user): add login functionality

Added login functionality that allows users to sign in with their email 
and password. This feature includes input validation and error handling.
```

#### 3. 푸터 (footer)

- **형식**: 한 줄 비워두고 작성
- **내용**: 관련된 이슈 번호, 참고 정보, 브레이킹 체인지 여부

**예시:**
```
feat(user): add login functionality

Added login functionality that allows users to sign in with their email 
and password. This feature includes input validation and error handling.

Resolves: #123
```

### Commit Message 타입

다양한 타입을 사용하여 변경 사항의 성격을 명확히 합니다. 다음은 자주 사용되는 타입입니다:

- **feat**: 새로운 기능 추가
- **fix**: 버그 수정
- **docs**: 문서 수정
- **style**: 코드 포맷팅, 세미콜론 누락 등, 코드 변경 없음
- **refactor**: 코드 리팩토링 (기능 변화 없음)
- **test**: 테스트 추가 또는 수정
- **chore**: 빌드 작업, 패키지 매니저 설정 등

**타입 예시:**
```
feat: 새로운 기능 추가
fix: 버그 수정
docs: 문서 수정
style: 코드 포맷팅
refactor: 코드 리팩토링
test: 테스트 추가
chore: 기타 변경 사항
```

### Commit Message 예시

**간단한 예시:**
```
fix(button): correct typo in class name
```

**자세한 예시:**
```
feat(auth): add JWT authentication

Implemented JSON Web Token (JWT) authentication to enhance security. 
Users can now log in using their credentials and receive a token for 
subsequent requests. This update also includes unit tests for the 
authentication module.

Resolves: #456
```

### Commit Message 작성 규칙

1. **현재 시제 사용**: "Add feature" (과거 시제 사용 금지)
2. **명령형 사용**: "Fix bug" (명령형으로 작성)
3. **적절한 타입 사용**: feat, fix, docs, style, refactor, test, chore 등
4. **관련 이슈 번호 포함**: 관련된 이슈 번호를 푸터에 포함
5. **일관성 유지**: 팀 내에서 합의된 형식을 일관되게 유지
