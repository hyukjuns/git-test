# log / restore / revert
```
# commit log
git log --oneline

# restore
파일 1개에 대한 실행취소, 복구
git restore <FILE>
git restore --source <COMMIT_ID> <FILE>

# 특정 파일 스테이징 취소
git restore --staged <FILE>

# revert
특정 커밋 취소(제거)
git revert <COMMIT_ID>

# 최근 커밋 1개 제거
git revert HEAD 
```

# Merge
```
# 3-way merge
메인과 브랜치를 비교해서 merge
(가장 일반적인 merge)

# fast-forward merge
메인에 변경사항(신규커밋)이 없을떄 브랜치의 커밋과 비교할게 없으므로, 브랜치의 커밋을 메인의 최신 커밋이 되도록 merge 하는 방식

# rebase and merge
브랜치의 시작점을 메인 브랜치(다른 브랜치)의 최신 커밋 다음으로 이어붙이고 fast-forward merge
(강제 fast-forward merge)

# squash and merge
브랜치의 모든 커밋 로그를 가져오지 않고 코드 변경사항만 메인으로 merge
(브랜치의 수많은 커밋을 하나의 커밋으로 새로 만들어서 메인 브랜치에 옮겨올 수 있음)
```