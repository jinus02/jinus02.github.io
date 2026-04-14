# 자소서 프로젝트

개인 자기소개서 홈페이지 — 영구 공개용 정적 사이트.

## 현재 상태
- [x] 프로젝트 폴더 생성
- [ ] 자소서 내용 PDF 업로드 (`content/` 폴더에 넣어주세요)
- [ ] 디자인 톤 결정
- [ ] index.html 제작
- [ ] GitHub repo 생성 + 배포
- [ ] GitHub Pages 공개

## 사용자가 해야 할 일

### 1. 자소서 내용 PDF 넣기
- 위치: `E:\지누스_프로젝트\projects\자소서프로젝트\content\`
- 파일명: 자유 (예: `자소서내용.pdf`)
- Claude가 읽어서 HTML에 반영합니다

### 2. GitHub 준비 (둘 중 택1)
**A) gh CLI 설치 (자동화 가능)**
```powershell
winget install --id GitHub.cli
gh auth login
```
설치 후 Claude가 `gh repo create` 로 repo 생성부터 배포까지 자동 진행

**B) 웹에서 수동 생성**
1. https://github.com/new 접속
2. Repository name: `<your-username>.github.io` (개인 홈페이지용 특수 이름)
3. Public 선택, README 추가 X
4. 생성된 repo URL을 Claude에게 알려주면 push 자동 진행

## 배포 경로
- **Host**: GitHub Pages (영구 무료)
- **URL**: `https://<your-username>.github.io`
- **SSL**: 자동 (Let's Encrypt)
- **커스텀 도메인**: 나중에 원하면 `zinus.kr` 등 구입 후 CNAME 연결 가능

## 구조 (예정)
```
자소서프로젝트/
├── README.md          (이 파일)
├── content/           (사용자가 PDF 넣는 곳)
│   └── 자소서내용.pdf
├── index.html         (메인 페이지)
├── style.css
├── assets/            (프로필 사진 등)
└── .gitignore
```
