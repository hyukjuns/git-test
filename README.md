### Cheatsheets
```markdown
# conflict
git merge BRANCH 후 특정 내용 충돌 시 필요한 내용만 남기고 git add & git commit (메시지 없이) 수행
혹은 git merge --abort 로 머지 작업 취소

# oh-my-zsh alias
gaa # git add -A
gc -m "message" # git commit -m "message"
gst # git status

# 최근 커밋 리셋 및 github 반영
git reset HEAD^
git push -f origin main

# commit log
git log
git log --oneline

# reset / revert / restore
git reset COMMIT_ID # 이전 상태로 되돌리기, 커밋 이력 삭제
git revert COMMIT_ID # 이전 상태로 되돌리기, 커밋 이력 유지, 신규 revert 커밋 이력 생성
git revert HEAD # 최근 커밋 1개 제거
git restore FILE # 파일 1개에 대한 실행취소, 복구
git restore --source COMMIT_ID FILE # 파일 1개에 대한 실행취소, 복구
git restore --staged FILE # 특정 파일 스테이징 취소

# branch / merge
git switch -c BRANCH # 브랜치 생성 및 이동
git switch BRANCH # 브랜치 이동
git branch -d BRANCH # 브랜치 제거
git branch  --list # 브랜치 목록
git merge BRANCH # 타겟 브랜치를 현재 브랜치로 머지

# 3-way merge
메인과 브랜치를 비교해서 merge (가장 일반적인 merge)

# fast-forward merge
메인에 변경사항(신규커밋)이 없을떄 브랜치의 커밋과 비교할게 없으므로, 브랜치의 커밋을 메인의 최신 커밋이 되도록 merge 하는 방식

# rebase and merge
브랜치의 시작점을 메인 브랜치(다른 브랜치)의 최신 커밋 다음으로 이어붙이고 fast-forward merge (강제 fast-forward merge)

# squash and merge
브랜치의 모든 커밋 로그를 가져오지 않고 코드 변경사항만 메인으로 merge
(브랜치의 수많은 커밋을 하나의 커밋으로 새로 만들어서 메인 브랜치에 옮겨올 수 있음)
```