# 가벼운 웹 UI (아이패드/폰용)

렌더링 없이 facts_db.json 확인·수정, 소재 상태 변경, Actions 실행만 합니다.

1. GitHub 토큰: Settings → Developer settings → Fine-grained tokens → 두 저장소 선택,
   권한 Contents: Read and write, Actions: Read and write
2. 새 GitHub 저장소(비공개)에 이 폴더의 web_ui.py, requirements.txt 업로드
3. share.streamlit.io → New app → 그 저장소, 메인 파일 web_ui.py
4. App settings → Secrets 에 입력:

```
GITHUB_TOKEN = "github_pat_..."
BRANCH = "main"
[REPOS]
"한국어" = "gonmau/한국어저장소이름"
"English" = "gonmau/영어저장소이름"
[WORKFLOWS]
"한국어" = "culture-shorts-pipeline.yml"
"English" = "korea-shorts-pipeline.yml"
```
5. 앱을 비공개로 하고(본인 계정만), 아이패드 사파리에서 열어 홈 화면에 추가
