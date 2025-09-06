# DewDew Snippets 빌드 가이드

## 📋 개요

DewDew Snippets는 프론트엔드 개발자를 위한 VS Code/Cursor 확장입니다. Vue3, Nuxt4, React, Next.js, React Native 스니펫을 제공합니다.

## 🛠️ 개발 환경 설정

### 1. 필수 도구 설치

```bash
# Node.js 설치 (v20.0.0 이상 권장)
node --version

# npm 설치 확인
npm --version

# vsce (Visual Studio Code Extension Manager) 설치
npm install -g vsce

# Open VSX CLI 설치 (선택사항)
npm install -g ovsx
```

### 2. 프로젝트 클론 및 의존성 설치

```bash
# 저장소 클론
git clone https://github.com/yeonjulee1005/dewdew-snippets.git
cd dewdew-snippets

# 의존성 설치
npm install
```

## 🔨 빌드 과정

### 1. 개발 모드

```bash
# TypeScript 컴파일 (한 번만)
npm run compile

# 감시 모드로 개발
npm run watch
```

### 2. 패키지 빌드

```bash
# 패키지 빌드
npm run package

# 또는 직접 vsce 사용
vsce package
```

### 3. 빌드 결과 확인

빌드가 성공하면 `dewdew-snippets-0.0.4.vsix` 파일이 생성됩니다.

## 📦 배포 과정

### 1. VS Code 마켓플레이스 배포

```bash
# vsce 로그인 (처음 한 번만)
vsce login DewdewSnippets

# 마켓플레이스에 출시
vsce publish

# 또는 npm 스크립트 사용
npm run publish
```

### 2. Open VSX Registry 배포

```bash
# Open VSX 로그인
ovsx login yeonjulee1005

# Open VSX에 출시
ovsx publish dewdew-snippets-0.0.4.vsix
```

### 3. 로컬 테스트

```bash
# VS Code에서 확장 설치 테스트
code --install-extension dewdew-snippets-0.0.4.vsix

# Cursor에서 확장 설치 테스트
cursor --install-extension dewdew-snippets-0.0.4.vsix
```

## 🔧 문제 해결

### 1. Cursor 호환성 문제

**문제**: Cursor에서 확장이 설치되지 않음
**해결**: `package.json`의 `engines` 필드 수정

```json
{
  "engines": {
    "vscode": "^1.60.0"
  },
  "devDependencies": {
    "@types/vscode": "^1.60.0"
  }
}
```

### 2. Publisher ID 불일치

**문제**: `Publisher ID 'DewdewSnippets' provided in the extension manifest should match the publisher ID 'DewdewSnippets'`
**해결**: `package.json`의 `publisher` 필드를 기존과 동일하게 설정

```json
{
  "publisher": "DewdewSnippets"
}
```

### 3. 이미지 표시 문제

**문제**: README.md의 이미지가 표시되지 않음
**해결**: GitHub raw URL 사용

```markdown
<img src="https://raw.githubusercontent.com/yeonjulee1005/dewdew-snippets/master/images/icon.png" width='180px' height='180px' alt="DewDew Snippets Icon">
```

## 📁 프로젝트 구조

```
dewdew-snippets/
├── images/
│   └── icon.png              # 확장 아이콘
├── snippets/
│   ├── vue3.code-snippets    # Vue3 스니펫
│   ├── nuxt4.code-snippets   # Nuxt4 스니펫
│   ├── react.code-snippets   # React 스니펫
│   ├── nextjs.code-snippets  # Next.js 스니펫
│   └── react-native.code-snippets # React Native 스니펫
├── package.json              # 확장 매니페스트
├── CHANGELOG.md              # 변경 로그
├── README.md                 # 프로젝트 문서
├── LICENSE                   # MIT 라이선스
└── SETUP.md                  # 이 파일
```

## 🚀 빠른 시작

```bash
# 1. 프로젝트 클론
git clone https://github.com/yeonjulee1005/dewdew-snippets.git
cd dewdew-snippets

# 2. 의존성 설치
npm install

# 3. 패키지 빌드
npm run package

# 4. 로컬 테스트
code --install-extension dewdew-snippets-0.0.4.vsix

# 5. 마켓플레이스 출시
vsce publish
```

## 📝 버전 관리

### 버전 업데이트

```bash
# 패치 버전 (0.0.3 → 0.0.4)
npm version patch

# 마이너 버전 (0.0.3 → 0.1.0)
npm version minor

# 메이저 버전 (0.0.3 → 1.0.0)
npm version major
```

### CHANGELOG 업데이트

새로운 버전을 출시할 때마다 `CHANGELOG.md`에 변경사항을 기록하세요.

## 🔍 디버깅

### 확장 로그 확인

```bash
# VS Code 개발자 도구 열기
# Help → Toggle Developer Tools → Console

# 확장 로그 확인
code --log trace
```

### 확장 재로드

```bash
# 명령 팔레트에서
# Ctrl+Shift+P (Windows/Linux) 또는 Cmd+Shift+P (Mac)
# "Developer: Reload Window" 실행
```

## 📚 유용한 명령어

```bash
# 패키지 정보 확인
vsce show

# 설치된 확장 목록 확인
code --list-extensions

# 특정 확장 제거
code --uninstall-extension DewdewSnippets.dewdew-snippets

# 확장 검증
vsce verify
```

## 🎯 다음 단계

1. **스니펫 추가**: `snippets/` 디렉토리에 새로운 스니펫 추가
2. **테스트**: 다양한 언어 파일에서 스니펫 동작 확인
3. **문서화**: README.md에 새로운 스니펫 사용법 추가
4. **출시**: 버전 업데이트 후 마켓플레이스에 출시

---

**문의사항이 있으시면 [GitHub Issues](https://github.com/yeonjulee1005/dewdew-snippets/issues)에 등록해주세요!** 🚀
