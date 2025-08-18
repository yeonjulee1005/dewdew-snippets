# DewDew Snippets

Vue3, Nuxt4, React, React Native, Next.js를 위한 유용한 코드 스니펫 모음입니다.

## 🚀 설치

마켓플레이스에서 "DewDew Snippets"를 검색하여 설치하거나, `.vsix` 파일을 다운로드하여 수동으로 설치할 수 있습니다.

## 📚 사용 가능한 스니펫

### Vue3 스니펫

| 접두사 | 설명 | 파일 |
|--------|------|------|
| `ddv3c` | Vue3 컴포지션 API 컴포넌트 | `snippets/vue3.code-snippets` |
| `ddv3p` | Vue3 피니아 스토어 | `snippets/vue3.code-snippets` |
| `ddv3r` | Vue3 라우터 네비게이우 | `snippets/vue3.code-snippets` |

### Nuxt4 스니펫

| 접두사 | 설명 | 파일 |
|--------|------|------|
| `ddn4p` | Nuxt4 페이지 | `snippets/nuxt4.code-snippets` |
| `ddn4l` | Nuxt4 레이아웃 | `snippets/nuxt4.code-snippets` |
| `ddn4c` | Nuxt4 컴포넌트 | `snippets/nuxt4.code-snippets` |
| `ddn4cp` | Nuxt4 컴포저블 | `snippets/nuxt4.code-snippets` |
| `ddn4sr` | Nuxt4 서버 라우트 | `snippets/nuxt4.code-snippets` |
| `ddn4m` | Nuxt4 미들웨어 | `snippets/nuxt4.code-snippets` |
| `ddn4pl` | Nuxt4 플러그인 | `snippets/nuxt4.code-snippets` |

// 완료 하단의 내용은 작업 예정

### React 스니펫

| 접두사 | 설명 | 파일 |
|--------|------|------|
| `ddrfc` | React 함수형 컴포넌트 | `snippets/react.code-snippets` |
| `ddrfch` | React 함수형 컴포넌트 + 훅 | `snippets/react.code-snippets` |
| `ddrcu` | React 커스텀 훅 | `snippets/react.code-snippets` |
| `ddrc` | React Context + Reducer | `snippets/react.code-snippets` |
| `ddrev` | React 이벤트 핸들러 | `snippets/react.code-snippets` |

### Next.js 스니펫

| 접두사 | 설명 | 파일 |
|--------|------|------|
| `next-app-page` | Next.js App Router 페이지 | `snippets/nextjs.code-snippets` |
| `next-app-layout` | Next.js App Router 레이아웃 | `snippets/nextjs.code-snippets` |
| `next-api` | Next.js API 라우트 | `snippets/nextjs.code-snippets` |
| `next-server` | Next.js 서버 컴포넌트 | `snippets/nextjs.code-snippets` |
| `next-client` | Next.js 클라이언트 컴포넌트 | `snippets/nextjs.code-snippets` |
| `next-image` | Next.js Image 컴포넌트 | `snippets/nextjs.code-snippets` |
| `next-link` | Next.js Link 컴포넌트 | `snippets/nextjs.code-snippets` |

### React Native 스니펫

| 접두사 | 설명 | 파일 |
|--------|------|------|
| `rnfc` | React Native 함수형 컴포넌트 | `snippets/react-native.code-snippets` |
| `rnscreen` | React Native 화면 컴포넌트 | `snippets/react-native.code-snippets` |
| `rnnav` | React Native 네비게이션 | `snippets/react-native.code-snippets` |
| `rnflatlist` | React Native FlatList | `snippets/react-native.code-snippets` |
| `rnbutton` | React Native 터치 가능한 버튼 | `snippets/react-native.code-snippets` |
| `rnstyle` | React Native StyleSheet | `snippets/react-native.code-snippets` |

## 💡 사용법

1. VS Code에서 해당 언어의 파일을 엽니다 (예: `.vue`, `.tsx`, `.js` 등)
2. 접두사를 입력하고 `Tab` 또는 `Enter`를 누릅니다
3. `$1`, `$2` 등의 플레이스홀더를 원하는 값으로 교체합니다

## 🔧 개발 및 빌드

### 의존성 설치
```bash
npm install
```

### 패키징
```bash
npm run package
```

### 배포
```bash
npm run publish
```

## 📝 스니펫 추가하기

새로운 스니펫을 추가하려면:

1. 해당 언어의 `.code-snippets` 파일을 편집합니다
2. JSON 형식으로 스니펫을 추가합니다
3. `package.json`의 `contributes.snippets` 섹션에 언어 매핑을 추가합니다

## 🤝 기여하기

버그 리포트, 기능 요청, 풀 리퀘스트를 환영합니다!

## 📄 라이선스

MIT License

## 🙏 감사의 말

이 스니펫 모음은 개발자들의 생산성 향상을 위해 만들어졌습니다. 유용하게 사용해 주세요!
