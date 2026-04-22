# 대항해시대2 - DOS 버전 웹 에뮬레이터

[js-dos](https://js-dos.com) v8을 사용해 브라우저에서 대항해시대2 (Uncharted Waters: New Horizons) DOS 버전을 실행합니다.

## 데모

GitHub Pages 배포 후: `https://UnopndJude.github.io/uncharted-waters-2-dos/`

## 로컬 실행

```bash
# 정적 서버 아무거나
python3 -m http.server 8000
# 또는
npx serve .
```

브라우저에서 `http://localhost:8000` 접속.

## 게임 파일 준비 (중요)

**저작권 문제로 이 레포는 게임 파일을 포함하지 않습니다.** 본인이 정식 보유한 게임 파일만 사용하세요.

1. 대항해시대2 DOS 버전 파일을 준비합니다 (`.zip` 또는 DOSBox로 실행 가능한 폴더)
2. [DOS Zone Studio](https://dos.zone/studio/)에서 `.jsdos` 번들로 패키징
3. 생성된 `game.jsdos` 파일을 프로젝트 루트에 배치
4. `.gitignore`에 의해 git에는 커밋되지 않음 (의도적)

## 구조

```
.
├── index.html              # js-dos 엔트리 포인트
├── game.jsdos              # (로컬 전용, 커밋 안 됨) 게임 번들
└── .github/workflows/      # GitHub Pages 자동 배포
```

## 저작권

- 이 레포의 **코드** 부분은 MIT 라이선스
- **대항해시대2 (Uncharted Waters: New Horizons)** 는 Koei Tecmo의 저작물입니다
- 이 프로젝트는 교육/연구/개인 소장 목적의 에뮬레이터 프론트엔드만 제공합니다
- 게임 파일 배포는 저작권 침해입니다 — 본인 소유 파일만 로컬에서 사용하세요

## 기술 스택

- [js-dos v8](https://v8.js-dos.com/latest/) — DOSBox의 WebAssembly 빌드
- GitHub Pages — 정적 호스팅
