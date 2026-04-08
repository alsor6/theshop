# 더샵플러스 새벽배송 동선 시뮬레이션

건물 폐쇄 시간을 고려한 약국 배송 동선 시뮬레이션 도구입니다.  
카카오맵 API를 사용하여 실제 도로 경로를 표시합니다.

## 🚀 배포 방법 (GitHub Pages)

### 1단계: API 키 입력

`index.html` 파일에서 아래 2곳의 키를 입력합니다.

**JavaScript 키** (169번째 줄 근처):
```
appkey=YOUR_JAVASCRIPT_KEY
```

**REST API 키** (300번째 줄 근처):
```javascript
const KAKAO_REST_KEY = 'YOUR_REST_API_KEY';
```

> 카카오 개발자 콘솔 > 내 애플리케이션 > 앱 키에서 확인

### 2단계: 카카오 플랫폼 등록

카카오 개발자 콘솔 > 내 애플리케이션 > 앱 설정 > 플랫폼 에서:

- **Web 플랫폼 등록** 클릭
- 사이트 도메인: `https://본인아이디.github.io`

### 3단계: GitHub 배포

```bash
git init
git add .
git commit -m "배송 동선 시뮬레이션"
git branch -M main
git remote add origin https://github.com/본인아이디/저장소이름.git
git push -u origin main
```

GitHub > 저장소 > Settings > Pages > Source를 `main` 브랜치로 설정

접속: `https://본인아이디.github.io/저장소이름/`

## 📋 기능

- 787개 백제약품 약국 전체 조회/검색
- 23개 동선검토처 (별도경로O/X 구분)
- 건물 폐쇄 시간 기반 배송 순서 자동 최적화
- 최대 차량 수 내에서 필요한 만큼만 자동 배정
- 카카오맵 실제 도로 경로 표시
