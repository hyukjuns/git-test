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
git log --oneline --graph

# reset / revert / restore
git reset COMMIT_ID # 이전 상태로 되돌리기, 커밋 이력 삭제
git revert COMMIT_ID # 이전 상태로 되돌리기, 커밋 이력 유지, 신규 revert 커밋 이력 생성
git revert HEAD # 최근 커밋 1개 제거
git restore FILE # 파일 1개에 대한 실행취소, 복구
git restore --source COMMIT_ID FILE # 특정 커밋 시점으로 파일 복구
git restore --staged FILE # 특정 파일 스테이징 취소

# branch / merge
git switch -c BRANCH # 브랜치 생성 및 이동
git switch BRANCH # 브랜치 이동
git branch -d BRANCH # Merge된 브랜치 제거
git branch -D BRANCH # Merge되지 않은 브랜치 제거
git branch  --list # 브랜치 목록
git merge BRANCH # 타겟 브랜치를 현재 브랜치로 머지

# 3-way merge
각 브랜치에 신규 커밋이 있을 경우 병합할 브랜치들의 코드를 비교하고 합쳐서 새로운 커밋을 생성, 가장 일반적인 merge
- git merge BRANCH
- git merge --no-ff BRANCH # 강제

# fast-forward merge
병합의 기분이 되는 메인브랜치에 신규커밋이 없을떄는
신규브랜치와 메인브랜치의 커밋을 비교하지 않아도 되므로, 
신규브랜치의 커밋을 메인브랜치의 최신 커밋이 되도록 병합 하는 방식
- git merge BRANCH

# rebase and merge
신규브랜치의 시작점을 메인브랜치의 최신 커밋 다음으로 이어붙힘
그 상태에서 fast-forward merge 즉, 강제 fast-forward merge
순서
1. git switch BRANCH
2. git rebase main
3. git switch main
4. git merge BRANCH

# squash and merge
메인브랜치로 병합시 신규브랜치의 모든 커밋을 가져오지 않고 모든 변경사항을 하나의 커밋으로 가져와서 메인브랜치와 병합시킴
- git merge --squash BRANCH
```