# Expected Questions

Organized expected questions & answers

## React Native (+HTML, CSS, Javascript, Typescript)

- React Native와 React의 차이점
  - 공통 사항
    - 둘 다 리액트 라이브러리 기반하나 사용 목적과 실행 환경에서의 차이
  - 개념 (React.js / React Native)
    - 설명
      - 웹 애플리케이션 개발을 위한 UI 라이브러리
      - 모바일 앱(Android/iOS) 개발을 위한 프레임워크
    - 실행 환경
      - 브라우저 (Chrome, Firefox 등)
      - 모바일 앱 (Android, iOS)
    - 렌더링 방식
      - HTML + CSS 사용
      - 네이티브 UI 컴포넌트 사용 (View, Text 등)
    - 사용 언어
      - JavaScript, JSX, CSS
      - JavaScript, JSX, 스타일은 React Native 스타일 객체 사용
    - 배포 방식
      - 웹사이트 URL로 접근
      - Android/iOS 앱스토어에 배포
  - 주요 차이점
    - UI 요소 (HTML vs 네이티브 컴포넌트)
	  - React는 웹을 위한 HTML 태그(div, span, button, input 등) 을 사용.
	  - React Native는 네이티브 모바일 UI 요소(View, Text, Button, ScrollView 등)를 사용.
    - 스타일링 방식 (CSS vs React Native Styles)
	  - React에서는 CSS 또는 CSS-in-JS 사용.
	  - React Native에서는 StyleSheet API를 사용하여 스타일 적용
    - 네비게이션 방식 (React Router vs React Navigation)
      - React (웹)에서는 react-router-dom을 사용하여 URL 기반 라우팅을 함
      - React Native (모바일)에서는 react-navigation을 사용하여 화면 간 이동을 처리.
  - API 접근 방식
    - React (웹)
	  - fetch 또는 axios로 API 호출
	  - 브라우저 기반 API 사용 (예: localStorage, sessionStorage, document 등)
    - React Native (모바일)
	  - fetch 또는 axios로 API 호출
	  - 네이티브 기능 접근 가능 (카메라, GPS, 센서 등)
	    - react-native-camera → 카메라 사용
	    - react-native-geolocation → GPS 사용
	    - AsyncStorage → 로컬 데이터 저장
  - 사용 목적에 따른 선택
    - 웹사이트 개발: 리액트
    - 모바일 앱 개발: 리액트 네이티브
    - 데스크톱 앱 개발: 리액트 (Electron 사용 가능)
    - 하이브리드 개발 (웹+앱): 리액트 (PWA 가능) / 리액트 네이티브 (크로스플랫폼 앱 가능)


- React Native에서 Navigation을 구현하는 방법은?
- React Native에서 상태 관리는 어떻게 하는가?
- React Native에서 AsyncStorage의 역할은?
- React Native에서 Reanimated란?
- React Native에서 Native Module이란?
- React Native에서 Expo와 Bare Workflow의 차이점은?
- React Native에서 성능 최적화 방법은?
- React Native에서 useEffect의 메모리 누수를 방지하는 방법은?
- React Native에서 Gesture Handling을 구현하는 방법은?
- React Native에서 push notification을 설정하는 방법은?
- React Native에서 App State를 관리하는 방법은?
- React Native에서 Hot Reloading과 Fast Refresh의 차이점은?
- React Native에서 Dynamic Linking이란?
- React Native에서 Code Splitting이 필요한 이유는?
- React Native에서 Flipper를 사용하는 이유는?
- React Native의 Metro Bundler와 Webpack의 차이점은?
- React Native에서 Hermes 엔진을 사용하는 장점은?
- React Native에서 SafeAreaView의 역할은?
- React Native에서 Dynamic Styles을 적용하는 방법은?
- React Native에서 Performance Profiling을 수행하는 방법은?
- React Native에서 Detox와 Appium의 차이점은?
- React Native에서 Firebase를 연동하는 방법은?
- React Native에서 Clipboard API를 사용하는 방법은?
- React Native에서 StatusBar를 동적으로 변경하는 방법은?
- React Native에서 Redux Toolkit을 사용하는 이유는?
- React Native에서 AsyncStorage와 SecureStore의 차이점은?
- React Native에서 React Navigation과 React Router의 차이점은?
- React Native에서 ScrollView와 FlatList의 차이점은?
- React Native에서 Dynamic Styles을 적용하는 방법은?
- React Native에서 Performance Profiling을 수행하는 방법은?
- React Native에서 Detox와 Appium의 차이점은?
- React Native에서 Firebase를 연동하는 방법은?
- React Native에서 Clipboard API를 사용하는 방법은?
- React Native에서 StatusBar를 동적으로 변경하는 방법은?
- React Native에서 Native Module을 직접 구현하는 방법은?
- React Native에서 Gesture Handler를 설정하는 방법은?
- React Native에서 Hermes의 주요 기능은?
- React Native에서 Expo를 사용할 때의 장단점은?
- React Native에서 Animated API를 활용한 애니메이션 구현 방법은?
- React Native에서 Deep Linking을 적용하는 방법은?
- React Native에서 AppState를 활용하는 방법은?
- React Native에서 SafeAreaView의 역할은?
- React Native에서 CodePush를 활용하여 앱을 배포하는 방법은?
- React Native에서 Splash Screen을 최적화하는 방법은?
- React Native에서 Background Task를 실행하는 방법은?
- React Native에서 WebSockets을 사용하는 방법은?
- React Native에서 Fast Refresh가 동작하는 방식은?
- React Native에서 TurboModules의 역할은?
- React Native에서 Flipper 디버깅 툴을 활용하는 방법은?
- React Native에서 Accessibility를 개선하는 방법은?
- React Native에서 Gesture Responder System이 동작하는 방식은?
- React Native에서 Firebase Firestore와 Realtime Database의 차이점은?
- React Native에서 Camera 기능을 구현하는 방법은?
- React Native에서 Dark Mode를 적용하는 방법은?
- React Native에서 Multi-Threading을 구현하는 방법은?
- React Native에서 React Query를 사용하는 이유는?
- React Native에서 WebView를 활용하는 방법은?
- React Native에서 Reanimated 라이브러리를 사용하는 방법은?
- React Native에서 Lottie를 활용한 애니메이션을 적용하는 방법은?
- React Native에서 Google Maps를 적용하는 방법은?
- React Native에서 Video Streaming을 구현하는 방법은?
- React Native에서 Native Bridge를 사용하는 이유는?
- React Native에서 Native Event Emitter의 역할은?
- React Native에서 터치 이벤트를 처리하는 방법은?
- React Native에서 Push Notification을 설정하는 방법은?
- React Native에서 Apple Pay와 Google Pay를 연동하는 방법은?
- React Native에서 환경 변수(.env) 파일을 사용하는 방법은?
- React Native에서 EAS(Expo Application Services)를 활용하는 방법은?
- React Native에서 앱 크기를 최적화하는 방법은?
- React Native에서 서버와의 실시간 동기화를 구현하는 방법은?
- React Native에서 File Upload 기능을 구현하는 방법은?
- React Native에서 Custom Fonts를 적용하는 방법은?
- React Native에서 Local Authentication(지문, 얼굴 인식)을 적용하는 방법은?
- React Native에서 Dynamic Linking이란 무엇인가?
- React Native에서 Third-Party 모듈을 효과적으로 관리하는 방법은?
- React Native에서 Multi-Platform을 위한 코드 구조화 방법은?
- React Native에서 MobX와 Redux의 차이점은?
- React Native에서 Accessibility를 최적화하는 방법은?
- React Native에서 WebView와 iframe의 차이점은?
- React Native에서 배터리 소모를 줄이기 위한 방법은?
- React Native에서 Bluetooth 기능을 구현하는 방법은?
- React Native에서 Offline Mode를 구현하는 방법은?
- React Native에서 앱에서 로그를 수집하는 방법은?
- React Native에서 AI 모델을 활용하는 방법은?
- React Native에서 Face Recognition을 적용하는 방법은?
- React Native에서 AsyncStorage의 대체 기술은?
- React Native에서 JWT 인증을 구현하는 방법은?
- React Native에서 Background Fetch를 활용하는 방법은?
- React Native에서 GraphQL을 활용한 데이터 관리 방법은?
- React Native에서 프로젝트 구조를 설계할 때 고려해야 할 사항은?
- React Native에서 백그라운드에서 앱이 실행되도록 유지하는 방법은?
- React Native에서 앱이 종료되었을 때도 알림을 받을 수 있도록 하는 방법은?
- React Native에서 CI/CD를 구축하는 방법은?
- React Native에서 Redux를 사용할 때 발생할 수 있는 문제점과 해결 방법은?
- React Native에서 Splash Screen이 오래 걸리는 문제를 해결하는 방법은?
- React Native에서 앱 로딩 속도를 개선하는 방법은?
- React Native에서 Expo에서 Bare Workflow로 마이그레이션하는 방법은?
- React Native에서 CI/CD 파이프라인을 구축하는 방법은?
- React Native에서 Custom Hooks를 효과적으로 활용하는 방법은?
- React Native에서 앱 실행 중 동적 모듈 로딩을 수행하는 방법은?
- React Native에서 Global State 관리를 위한 최적의 방법은?
- React Native에서 Navigation 상태를 동적으로 관리하는 방법은?
- React Native에서 AI 기반 음성 인식 기능을 추가하는 방법은?
- React Native에서 Flutter와 비교했을 때의 장점은?
- React Native에서 Expo Managed Workflow와 Bare Workflow의 차이점은?
- React Native에서 Google Sign-In을 적용하는 방법은?
- React Native에서 WebRTC를 활용한 영상 통화를 구현하는 방법은?
- React Native에서 프로젝트를 TypeScript로 마이그레이션하는 방법은?
- React Native에서 UI 성능을 개선하는 방법은?
- React Native에서 FlatList의 성능 최적화를 위해 고려해야 할 점은?
- React Native에서 AsyncStorage의 데이터를 암호화하는 방법은?
- React Native에서 프로젝트에서 코드 스플리팅을 적용하는 방법은?
- React Native에서 Internationalization(다국어 지원)을 구현하는 방법은?
- React Native에서 앱을 A/B 테스트하는 방법은?
- React Native에서 In-App Purchase를 구현하는 방법은?
- React Native에서 Expo Go를 활용하는 방법은?
- React Native에서 Apple의 App Tracking Transparency(ATT)를 적용하는 방법은?
- React Native에서 UI/UX를 개선하는 방법은?
- React Native에서 GPU 성능 최적화를 수행하는 방법은?
- React Native에서 Security Vulnerability를 해결하는 방법은?
- React Native에서 Context API를 Redux 대체제로 사용하는 방법은?
- React Native에서 Navigation Stack을 효율적으로 관리하는 방법은?
- React Native에서 Native Code와의 통신을 최적화하는 방법은?
- React Native에서 Jetpack Compose와의 연동 방법은?
- React Native에서 JSI(JavaScript Interface)의 역할과 활용 방법은?
- React Native에서 Fabric Renderer의 개념과 기존 Bridge와의 차이점은?
- React Native에서 TurboModules의 동작 원리와 성능 개선 방법은?
- React Native에서 Hermes 엔진을 사용하는 이유는?
- React Native와 Native 개발의 차이점은 무엇인가요?
- React Native에서의 성능 최적화 방법을 설명해주세요.
- React Native의 Bridge와 TurboModules에 대해 설명해주세요.
- React Native의 Hermes 엔진 사용 경험을 설명해주세요.
- React Native의 JSI(JavaScript Interface)와 Fabric 아키텍처에 대해 설명해주세요.
- React Native에서 Fabric과 기존 렌더링 방식의 차이점은?
- React Native에서 Metro Bundler와 Webpack의 차이점은?
- React Native에서 Gesture Handler를 최적화하는 방법은?
- React Native에서 Dynamic Code Push를 적용하는 방법은?
- React Native에서 Hermes 엔진을 사용할 때의 장점은?
- React Native에서 Accessibility를 최적화하는 방법은?
- React Native에서 Custom Native Module을 작성하는 방법은?
- React Native와 Flutter의 차이점은?
- React Native에서 native module을 추가하는 방법은?
- React Native에서 성능 최적화를 위해 어떤 기법을 적용하는가?
- React Native의 useEffect가 componentDidMount와 componentWillUnmount와 어떻게 비교되는가?
- React Native에서 AsyncStorage와 SecureStore의 차이는?
- React Native에서 Animation을 구현하는 방법은?
- React Native에서 네이티브 코드(Android, iOS)와 연동하는 방법은?
- React Native에서 TurboModules와 Fabric의 개념을 설명하라.
- React Native에서 JSC와 Hermes 엔진의 차이는?
- React Native의 Flipper 디버깅 도구를 활용하는 방법은?
- React Native에서 네이티브 모듈을 직접 구현할 때 주의해야 할 사항은?
- React Native의 Bridge 통신 방식과 성능 최적화 기법은?
- React Native의 기본 개념 및 차이점
- React Native에서 Virtual DOM이 어떻게 작동하는가?
- React Native의 JSX와 HTML의 차이점은?
- React Native의 View, Text, Image와 같은 기본 컴포넌트는 어떻게 동작하는가?
- React Native에서 DOM이 없는 환경에서 스타일을 어떻게 적용하는가?
- React Native에서 CSS 대신 StyleSheet.create를 사용하는 이유는?
- React와 React Native에서 onClick과 onPress 이벤트의 차이점은?
- React Native에서 iOS와 Android의 네이티브 코드 차이를 어떻게 다루는가?
- React Native에서 상태 관리를 위한 다양한 방법(Redux, Recoil, Zustand, MobX 등)을 비교해보세요.
- React Native에서 Context API와 Redux를 비교하고, 언제 Context API를 사용할지 설명하세요.
- React Native에서 useReducer를 상태 관리에 활용하는 방법은?
- React Native에서 상태 관리를 최적화하는 방법은? (e.g., 불필요한 리렌더링 방지)
- React Native에서 React.memo와 useMemo의 차이점과 사용 사례는?
- React Native에서 React Query와 SWR을 사용할 때의 차이점은?
- React Native에서 fetch API와 Axios의 차이점은?
- React Native에서 WebSocket과 HTTP Polling의 차이점은?
- React Native에서 GraphQL을 활용하는 방법은?
- React Native에서 API 호출을 최적화하는 방법은? (e.g., 캐싱, 중복 요청 방지)
- React Native에서 Background Fetch와 Foreground Fetch의 차이는?
- React Native에서 Long Polling을 구현하는 방법은?
- React Native에서 메모리 누수를 방지하는 방법은?
- React Native에서 Lazy Loading을 적용하는 방법은?
- React Native에서 앱 크기를 줄이는 방법은?
- React Native에서 FlatList의 getItemLayout을 활용하는 방법은?
- React Native에서 Animated API와 Reanimated의 차이점은?
- React Native에서 Fast Refresh가 어떻게 동작하는가?
- React Native에서 Hermes를 사용할 때 성능 이점은?
- React Native에서 Metro Bundler의 역할과 최적화 방법은?
- React Native에서 JavaScript 코드와 네이티브 코드가 어떻게 통신하는가?
- React Native에서 Custom Native Module을 구현하는 방법은?
- React Native에서 TurboModules와 기존 Native Module의 차이점은?
- React Native에서 Fabric Renderer가 기존 브릿지 방식과 어떻게 다른가?
- React Native에서 Native Event Emitter를 활용하는 이유는?
- React Native에서 Bluetooth 통신을 구현하는 방법은?
- React Native에서 react-native link와 autolinking의 차이점은?
- React Native에서 OAuth를 구현하는 방법은?
- React Native에서 JWT 토큰을 안전하게 저장하는 방법은?
- React Native에서 SecureStore와 AsyncStorage의 차이점은?
- React Native에서 Code Injection을 방지하는 방법은?
- React Native에서 App Transport Security (ATS)를 활성화하는 방법은?
- React Native에서 WebView 보안을 강화하는 방법은?
- React Native에서 Unit Test와 E2E Test를 수행하는 방법은?
- React Native에서 Jest와 Detox의 차이점은?
- React Native에서 CodePush를 활용하여 앱을 업데이트하는 방법은?
- React Native에서 App Store와 Google Play 배포 프로세스를 설명하세요.
- React Native에서 CI/CD 파이프라인을 구축하는 방법은?
- React Native에서 Firebase Test Lab을 활용하는 방법은?
- React Native에서 크래시 리포팅을 설정하는 방법은?
- React Native에서 SQLite와 Realm의 차이점은?
- React Native에서 AsyncStorage 대신 사용할 수 있는 데이터 저장 방법은?
- React Native에서 데이터를 암호화하는 방법은?
- React Native에서 실시간 동기화를 구현하는 방법은? (Firebase, WebSockets 등)
- React Native에서 Redux Persist와 MMKV의 차이점은?
- React Native에서 Apollo Client를 사용할 때의 장점은?
- React Native에서 i18n(다국어 지원)을 구현하는 방법은?
- React Native에서 Dynamic Font Scaling을 적용하는 방법은?
- React Native에서 Accessibility(접근성)를 강화하는 방법은?
- React Native에서 RTL (Right-to-Left) 언어를 지원하는 방법은?
- React Native에서 카메라와 갤러리를 사용하는 방법은?
- React Native에서 Face ID와 Touch ID를 적용하는 방법은?
- React Native에서 NFC 기능을 구현하는 방법은?
- React Native에서 GPS 및 위치 기반 서비스를 구현하는 방법은?
- React Native에서 AR(Augmented Reality) 기능을 적용하는 방법은?
- React Native에서 머신러닝 모델을 활용하는 방법은? (TensorFlow.js, ML Kit 등)
- React Native의 최신 트렌드 및 업데이트된 기능은 무엇인가?
- React Native에서 New Architecture(Fabric & TurboModules)를 적용하는 방법은?
- React Native와 Flutter를 비교할 때, React Native의 강점과 약점은?
- React Native의 JSI(JavaScript Interface)는 무엇이며, 어떻게 동작하는가?
- React Native에서 Expo Router를 사용하면 어떤 장점이 있는가?
- React Native에서 새로운 패키지를 선택할 때 고려해야 할 점은?