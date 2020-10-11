---
tags: tip
title: 좆같이 시끄럽네, 집어쳐 난 포기다.
id: 다-좆까-시끄러
note: 이거는 항상 마지막에 있어야 함, 그래서 이름 수정하고 재정렬할 필요 없도록 오더가 20임
order: 20
---

```git
cd ..
sudo rm -r fucking-git-repo-dir
git clone https://some.github.url/fucking-git-repo-dir.git
cd fucking-git-repo-dir
```

Eric V 이거 ㄳ. 이 농담이 `sudo`를 쓰는 거에 대한 모든 불평은 그남의 몫임


근데 진심, 니 브랜치가 완전 좆됐고 "git 이 허락하신" 방법 하에선 걍 니 리포 현재 상태를 리모트 리포 상태로 리셋밖엔 각이 안 안 나올 땐, 걍 해봐, 근데 파괴적이고 돌이킬 수 없는 방법임은 알아 두길 바람!!

```git
# 오리진의 마지막 스태이트를 가져옴
git fetch origin
git checkout master
git reset --hard origin/master
# 트랙되지 않은 파일과 폴더들을 지움
git clean -d --force
# 각각의 엉망인 브랜치에 checkout/reset/clean 을 반복
```