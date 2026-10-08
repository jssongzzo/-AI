# 수학 오답노트 AI PWA

## 주요 기능
1. 시험/문제 사진 촬영 및 업로드
2. 빨강/파랑 계열 채점 표시 제거
3. 손가락 브러시로 학생 답/표시 수동 제거
4. 채점된 사진 여러 장에서 빨간 표시 주변을 오답 후보로 자동 추출
5. 오답 후보 확인 및 삭제/선택
6. 오답노트 자동 구성
7. 브라우저 인쇄 기능을 이용한 PDF 저장
8. 선택한 오답 사진을 휴대폰 공유 기능으로 ChatGPT에 전달
9. ChatGPT 분석용 한국어 프롬프트 자동 포함
10. 별도 AI 서버/API 키 불필요

## GitHub Pages 배포
1. GitHub에서 새 repository를 만듭니다.
2. 이 폴더의 파일을 repository 루트에 업로드합니다.
3. Settings → Pages → Deploy from a branch → main / root를 선택합니다.
4. 생성된 GitHub Pages 주소를 iPhone Safari에서 엽니다.
5. Safari 공유 → 홈 화면에 추가하면 PWA처럼 사용할 수 있습니다.

## ChatGPT 연결 방식
PWA가 OpenAI API를 직접 호출하지 않습니다. 선택한 이미지 파일과 분석 프롬프트를 `navigator.share()`로 휴대폰 공유 시트에 전달합니다. iPhone/Android 및 ChatGPT 앱 버전에 따라 공유 대상으로 ChatGPT가 표시될 수 있습니다. 표시되지 않으면 ChatGPT 앱을 열고 같은 이미지를 직접 첨부하면 됩니다.

## 중요한 제한
- 브라우저만으로 OCR/수식인식/학생 답과 인쇄된 답의 완벽한 구분은 어렵습니다.
- 빨간 채점 표시를 기준으로 오답 후보를 찾는 휴리스틱이므로 결과 확인이 필요합니다.
- PDF는 브라우저의 인쇄 → PDF 저장 기능을 사용합니다.
- ChatGPT의 실제 문제 판독과 오답 분석은 ChatGPT 앱에서 수행됩니다.
