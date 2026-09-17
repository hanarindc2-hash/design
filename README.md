# design

Codex와 여러 컴퓨터에서 이어서 작업하기 위한 GitHub 기반 프로젝트 저장소입니다.

## 기본 사용 흐름

### 처음 사용하는 컴퓨터
```bash
git clone https://github.com/hanarindc2-hash/design.git
cd design
```

그 다음 Codex에서 이 폴더를 프로젝트/작업 폴더로 엽니다.

### 작업 시작 전
```bash
git pull
```

### 작업을 마친 후
```bash
git add .
git commit -m "작업 내용 요약"
git push
```

다른 컴퓨터에서는 다시 `git pull` 하면 최신 파일을 받아 이어서 작업할 수 있습니다.

## 구조

```text
design/
├─ AGENTS.md          # Codex가 읽을 프로젝트 작업 지침
├─ README.md          # 사람을 위한 프로젝트 설명
├─ .gitignore         # Git에 올리지 않을 파일
├─ .env.example       # 환경변수 이름 예시 (실제 비밀값 금지)
└─ src/               # 실제 작업 파일
```

## 보안

- `.env` 파일은 Git에 올리지 않습니다.
- API key, token, password 같은 비밀값은 커밋하지 않습니다.
- 현재 저장소는 Public이므로 공개되어도 되는 파일만 저장하세요.
