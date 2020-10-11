---
tags: tip
title: 젠장, 나 실수로 브랜치에 커밋할거 마스트에 커밋해버림!
id: 실수로-마스터-커밋
order: 4
---

```git
# 현재 마스터에서 새 브랜치 만들기
git branch some-new-branch-name
# 마스터 가장 최근 커밋 삭제
git reset HEAD~ --hard
git checkout some-new-branch-name
# 니 커밋 이제 새 브랜치에 있음 :)
```

참고: 이미 퍼블릭/공유 브랜치로 푸시해 버렸으면 이 방법 못 씀. 그리고 다른 방법 이미 시도한 후라면, `git reset HEAD@{number-of-commits-back}` 를 `HEAD~` 대신 해야 할 수도 있음. 무한한 슬픔. 그리고, 마아아아아아아안은 사람들이 내가 몰랐던 이 간단한 방법을 추천해줌. 모두 감사!