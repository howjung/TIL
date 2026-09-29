# Git / GitHub 핵심 명령어 정리

## 1. 프로젝트 최초 시작 및 푸시 (처음 만들었을 때)
- `git init` : 현재 폴더를 Git 저장소로 초기화
- `git add .` : 폴더 내 모든 파일 및 변경사항을 Git 대기 상태로 추가
- `git commit -m "feat: 첫 번째 커밋"` : 설명 메시지와 함께 변경사항 저장 (첫 커밋)
- `git branch -M main` : 기본 브랜치 이름을 main으로 설정
- `git remote add origin https://github.com/howjung/저장소이름.git` : GitHub 원격 저장소 URL 연결
- `git push -u origin main` : 작성한 커밋을 GitHub 원격 저장소로 최종 업로드

## 2. 일상적인 수정 및 업로드 (가장 자주 쓰는 3단계)
- `git status` : 현재 수정되거나 변경된 파일 상태 확인
- `git add .` : 변경된 모든 파일을 커밋 대기 상태로 올리기
- `git commit -m "feat: 기능 수정 및 추가"` : 변경 이유를 적은 메시지와 함께 커밋 생성 (잔디 심기)
- `git push` : 내 컴퓨터의 커밋 내역을 GitHub 저장소로 업로드

## 3. 기타 유용한 명령어
- `git pull` : GitHub 원격 저장소의 최신 코드를 내 컴퓨터로 받아오기
- `git log --oneline` : 지금까지 작성한 커밋 기록들을 한 줄씩 간결하게 보기
- `git remote -v` : 현재 연결되어 있는 GitHub 원격 저장소 주소 확인하기
- `git restore --staged .` : `git add`로 올렸던 대기 상태 취소하기
