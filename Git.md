# Git

### 1. Git 설치 및 설정

**1.1 Git 설치**
- [Git 공식 사이트](https://git-scm.com/)에서 운영체제에 맞는 설치 파일을 다운로드하여 설치합니다.

**1.2 Git 설정**
- 사용자 이름과 이메일을 설정합니다. 이 정보는 커밋 메시지에 사용됩니다.
  ```bash
  git config --global user.name "Your Name"
  git config --global user.email "your.email@example.com"
  ```

- Git 설정을 확인합니다.
  ```bash
  git config --list
  ```

### 2. Git 저장소 초기화 및 클론

**2.1 Git 저장소 초기화**
- 새로운 Git 저장소를 생성합니다. 현재 디렉토리를 Git 저장소로 초기화합니다.
  ```bash
  git init
  ```

**2.2 기존 저장소 클론**
- 기존 원격 저장소를 로컬로 복제합니다.
  ```bash
  git clone <repository_url>
  ```

### 3. 파일 상태 및 작업 관리

**3.1 파일 상태 확인**
- 작업 디렉토리의 파일 상태를 확인합니다.
  ```bash
  git status
  ```

**3.2 파일 추적 및 스테이징**
- 새 파일을 스테이징 영역에 추가합니다.
  ```bash
  git add <file_name>
  ```
- 변경된 모든 파일을 스테이징 영역에 추가합니다.
  ```bash
  git add .
  ```

**3.3 파일 변경 사항 보기**
- 파일의 변경 내용을 확인합니다.
  ```bash
  git diff
  ```

- 스테이징된 파일의 변경 내용을 확인합니다.
  ```bash
  git diff --staged
  ```

### 4. 커밋

**4.1 커밋 생성**
- 스테이징 영역의 변경 사항을 커밋합니다.
  ```bash
  git commit -m "Commit message"
  ```

**4.2 커밋 메시지 수정**
- 마지막 커밋 메시지를 수정합니다.
  ```bash
  git commit --amend -m "New commit message"
  ```

### 5. 브랜치

**5.1 브랜치 생성 및 이동**
- 새로운 브랜치를 생성하고 이동합니다.
  ```bash
  git checkout -b <branch_name>
  ```

**5.2 브랜치 목록 확인**
- 브랜치 목록을 확인합니다.
  ```bash
  git branch
  ```

**5.3 브랜치 전환**
- 다른 브랜치로 전환합니다.
  ```bash
  git checkout <branch_name>
  ```

**5.4 브랜치 삭제**
- 로컬 브랜치를 삭제합니다.
  ```bash
  git branch -d <branch_name>
  ```

- 강제로 로컬 브랜치를 삭제합니다.
  ```bash
  git branch -D <branch_name>
  ```

### 6. 병합 및 충돌 해결

**6.1 브랜치 병합**
- 현재 브랜치에 다른 브랜치를 병합합니다.
  ```bash
  git merge <branch_name>
  ```

**6.2 병합 충돌 해결**
- 충돌이 발생한 파일을 수동으로 수정하고, 충돌 해결을 완료합니다.
  ```bash
  git add <resolved_file>
  git commit -m "Resolve merge conflict"
  ```

### 7. 원격 저장소

**7.1 원격 저장소 추가**
- 원격 저장소를 추가합니다.
  ```bash
  git remote add origin <repository_url>
  ```

**7.2 원격 저장소 확인**
- 원격 저장소 목록을 확인합니다.
  ```bash
  git remote -v
  ```

**7.3 원격 저장소에서 변경 사항 가져오기**
- 원격 저장소의 변경 사항을 가져옵니다.
  ```bash
  git fetch origin
  ```

**7.4 원격 저장소와 동기화**
- 원격 저장소의 변경 사항을 병합합니다.
  ```bash
  git pull origin <branch_name>
  ```

**7.5 원격 저장소로 푸시**
- 로컬 변경 사항을 원격 저장소에 푸시합니다.
  ```bash
  git push origin <branch_name>
  ```

### 8. 되돌리기 및 리셋

**8.1 파일 되돌리기**
- 작업 디렉토리에서 파일을 되돌립니다.
  ```bash
  git checkout -- <file_name>
  ```

**8.2 커밋 되돌리기**
- 특정 커밋으로 되돌립니다.
  ```bash
  git revert <commit_hash>
  ```

**8.3 리셋**
- 마지막 커밋을 취소하고 변경 사항을 스테이징 영역에 남겨둡니다.
  ```bash
  git reset --soft HEAD^
  ```

- 마지막 커밋을 취소하고 변경 사항을 작업 디렉토리에 남겨둡니다.
  ```bash
  git reset --mixed HEAD^
  ```

- 마지막 커밋을 취소하고 변경 사항을 제거합니다.
  ```bash
  git reset --hard HEAD^
  ```

### 9. 기타 유용한 명령어

**9.1 로그 보기**
- 커밋 로그를 확인합니다.
  ```bash
  git log
  ```

- 간결한 형식의 커밋 로그를 확인합니다.
  ```bash
  git log --oneline
  ```

**9.2 태그**
- 태그를 생성합니다.
  ```bash
  git tag <tag_name>
  ```

- 태그를 푸시합니다.
  ```bash
  git push origin <tag_name>
  ```

- 모든 태그를 푸시합니다.
  ```bash
  git push origin --tags
  ```
