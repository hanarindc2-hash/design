# AGENTS.md

이 저장소는 여러 컴퓨터에서 Codex 작업을 이어가기 위한 공용 프로젝트 저장소다.

## Codex 작업 원칙

1. 작업을 시작하기 전에 현재 저장소의 구조와 README를 먼저 확인한다.
2. 사용자가 명시적으로 요청하지 않은 대규모 리팩터링은 피한다.
3. 기존 파일을 삭제하거나 덮어쓰기 전에 변경 범위를 확인한다.
4. 비밀값(API key, token, password, 개인 인증정보)은 저장소에 기록하지 않는다.
5. `.env` 실파일은 커밋하지 않고, 필요한 변수 이름만 `.env.example`에 기록한다.
6. 코드 변경 시 가능한 경우 실행/테스트 방법을 README 또는 관련 문서에 반영한다.
7. 새 컴퓨터에서 작업할 때는 먼저 `git pull`로 최신 상태를 동기화한다.
8. 작업 완료 후 변경사항을 검토하고 의미 있는 단위로 commit 한다.

## 권장 폴더 역할

- `src/`: 실제 프로젝트 코드 및 작업 파일
- `docs/`: 기획서, 메모, 설계 문서
- `assets/`: 이미지 등 프로젝트 리소스
- `scripts/`: 반복 작업 자동화 스크립트

## 다른 컴퓨터에서 이어서 작업하는 방법

```bash
git clone https://github.com/hanarindc2-hash/design.git
cd design
```

이미 clone 되어 있다면:

```bash
git pull
```

작업 후:

```bash
git add .
git commit -m "Describe changes"
git push
```

## 주의

현재 저장소가 Public 상태라면 공개되어도 되는 자료만 저장한다. 민감한 프로젝트를 다룰 경우 GitHub에서 저장소 Visibility를 Private으로 변경한 뒤 사용한다.
