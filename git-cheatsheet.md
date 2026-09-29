# Git / GitHub 핵심 명령어 정리

## 1. 프로젝트 최초 시작 및 푸시
git init
git add .
git commit -m "feat: 첫 번째 커밋"
git branch -M main
git remote add origin 저장소주소
git push -u origin main

## 2. 일상적인 수정 및 업로드 (자주 쓰는 3단계)
git status    # 변경 사항 확인
git add .     # 변경된 모든 파일 추가
git commit -m "feat: 수정 내용 작성"
git push      # GitHub에 푸시

## 3. 기타 유용한 명령어
git pull                   # GitHub 최신 코드 받아오기
git log --oneline          # 커밋 기록 보기
git remote -v              # 연결된 원격 저장소 주소 확인
git restore --staged .     # git add 취소
