---
tags: tip
title: 이런, 실수로 잘못된 브랜치에 커밋함!
id: 실수로-잘못된-브랜치-커밋
order: 5
---

```git
# 마지막 커밋 되돌리기, 하지만 수정은 커밋 가능한 상태로 보관
git reset HEAD~ --soft
git stash
# 현재 브랜치로 이동
git checkout name-of-the-correct-branch
git stash pop
git add . # or add individual files
git commit -m "your message here";
# 이제 수정사항이 올바른 브랜치에 있음
```

많은 사람들이 이 상황에 `cherry-pick` 쓰는 방법을 역시 추천했으니, 뭐든 당신한테 제일 말 되 보이는 걸로 고르길!

```git
git checkout name-of-the-correct-branch
# 마스터 마지막 커밋 고르기
git cherry-pick master
# 마스터에서 마지막 커밋 지우기
git checkout master
git reset HEAD~ --hard
```