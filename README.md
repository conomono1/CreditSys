# 신용공여 심사 시스템 v10 (단일파일)

GitHub에 올려서 배포·공유하기 위한 최소 구성입니다. **HTML 한 파일**에 고객 병합 데이터, 담보 위험도, DART 번들, 협의금리 이력 CSV가 포함되어 있습니다.

## 포함 파일

| 파일 | 설명 |
|------|------|
| `신용공여_심사_시스템_v10_단일파일.html` | 실행·데이터 통합본 (브라우저로 열기) |

## 사용 방법

1. 위 HTML 파일을 더블클릭하거나 브라우저로 드래그해 엽니다.
2. **Chart.js**와 **Google Fonts**는 CDN을 사용합니다. 첫 실행 시 인터넷 연결이 필요할 수 있습니다.
3. 사용 중 저장되는 내용(브라우저 localStorage 등)은 **이 HTML 파일 안에 자동으로 들어가지 않습니다.** 백업이 필요하면 앱의 보내기 기능을 사용하세요.

## GitHub 업로드

```bash
cd creditsys-v10-github
git init
git add .
git commit -m "Add credit screening system v10 single-file bundle"
git branch -M main
git remote add origin https://github.com/<conomono1>/<CreditSys>.git
git push -u origin main
```

GitHub 웹에서 **New repository**로 빈 저장소를 만든 뒤, 위 `<사용자명>`·`<저장소명>`을 바꿔서 실행하면 됩니다.

## 데이터 갱신

단일파일은 **생성 시점**의 데이터 스냅샷입니다. 병합 스크립트로 `.js` / `.csv`를 다시 만든 뒤 단일파일을 재생성했다면, 이 폴더의 HTML을 교체하고 다시 커밋하세요.

## 라이선스

이 저장소에 올리는 코드·데이터의 라이선스는 조직 정책에 맞게 별도로 명시하세요.
