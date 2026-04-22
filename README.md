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

### 방법 0: 웹만으로 올리기 (Git 설치 없음)

1. 브라우저에서 [https://github.com](https://github.com) 로그인.
2. 오른쪽 위 **+** → **New repository** → 저장소 이름 입력 → **Create repository**.
3. 새 저장소 페이지가 열리면 **uploading an existing file** 링크를 누르거나, 상단 **Add file** → **Upload files**.
4. 탐색기에서 이 폴더(`creditsys-v10-github`)를 연 뒤, 아래 **세 파일을 같이** 끌어다 놓기(또는 **choose your files**로 선택):
   - `신용공여_심사_시스템_v10_단일파일.html`
   - `README.md`
   - `.gitignore`
5. 아래 **Commit changes**를 눌러 저장.

**용량:** 한 파일당 약 **25MB 이하**만 웹 업로드가 됩니다. 이 HTML(~4MB)은 문제 없는 크기입니다. 그보다 크면 Git LFS나 Desktop·`git`을 써야 합니다.

**이름이 깨져 보이면:** 업로드 후 GitHub에서 파일명이 이상하면, 웹에서 해당 파일을 연 뒤 **이름 변경(연필 아이콘)**으로 다시 저장해 보세요.

---

**PC에 Git이 없으면** 아래 **방법 1** 명령은 동작하지 않습니다. 웹만 쓰려면 위 **방법 0**으로 충분합니다.

### 사전 확인 (PowerShell)

```powershell
git --version
```

- **오류·인식 안 됨** → [Git for Windows](https://git-scm.com/download/win) 설치 후, 터미널을 **완전히 닫았다가** 다시 연 다음 같은 폴더에서 진행하세요.
- **버전이 출력됨** → 아래 **방법 1** 사용 가능.

### 방법 1: 명령줄 (Git 설치 후)

1. GitHub 웹 → **New repository** → 저장소 이름만 정하고 **README 추가는 하지 않은 빈 저장소**로 만듭니다.
2. PowerShell에서 **이 폴더의 전체 경로**로 이동합니다. (예시, 본인 PC 경로에 맞게 수정)

```powershell
cd "c:\Users\ahik2\Downloads\ai\새 폴더 (5)\바탕화면\creditsys-v10-github"
git init
git add .
git commit -m "Add credit screening system v10 single-file bundle"
git branch -M main
git remote add origin https://github.com/<사용자명>/<저장소명>.git
git push -u origin main
```

3. `<사용자명>`·`<저장소명>`을 본인 GitHub 계정·방금 만든 저장소 이름으로 바꿉니다.
4. `git push`에서 로그인을 요구하면 GitHub는 비밀번호 대신 **Personal Access Token**을 씁니다. ([토큰 만들기 안내](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/managing-your-personal-access-tokens))

**참고:** GitHub가 빈 저장소 안내에 `…git remote add origin…`을 이미 보여준 경우, `git remote add`를 두 번 하면 오류가 납니다. 그때는 `git remote remove origin` 후 다시 추가하거나, 이미 있다면 `git remote add` 줄은 건너뜁니다.

### 방법 2: GitHub Desktop (명령줄 없이)

1. [GitHub Desktop](https://desktop.github.com/) 설치 후 실행합니다.
2. **File → Add local repository**가 아니라, 처음이면 **File → New repository**로 이 폴더(`creditsys-v10-github`)를 지정하거나, **기존 폴더를 저장소로 추가**한 뒤 커밋합니다.
3. 상단 **Publish repository**로 GitHub에 올립니다. (웹에서 빈 저장소를 미리 만들었으면 **Repository → Repository settings → Remote**에서 URL을 맞춰도 됩니다.)

큰 파일(수십 MB 이상)은 웹 업로드 제한이 있을 수 있어, 그때는 **GitHub Desktop**이나 **방법 1**을 쓰는 편이 낫습니다.

## 데이터 갱신

단일파일은 **생성 시점**의 데이터 스냅샷입니다. 병합 스크립트로 `.js` / `.csv`를 다시 만든 뒤 단일파일을 재생성했다면, 이 폴더의 HTML을 교체하고 다시 커밋하세요.

## 라이선스

이 저장소에 올리는 코드·데이터의 라이선스는 조직 정책에 맞게 별도로 명시하세요.
