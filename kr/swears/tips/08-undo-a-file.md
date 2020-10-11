---
tags: tip
title: 젠장, 파일 하나의 수정 사항을 전부 되돌려야 해!
id: 파일-하나-되돌리기
order: 8
---

```git
# 파일이 수정된 커밋 전의 스태시 찾기
git log
# 화살표키로 기록을 오르내릴 수 있음
# 커밋을 찾았으면, 스태시에 저장함
git checkout [saved hash] -- path/to/file
# 예전 버전의 파일이 이제 인덱스에 있게 됨
git commit -m "Wow, you don't have to copy-paste to undo"
```

내가 마침내 이 방법을 찾아 냈을 때 ㄷㄷㄷㄷㄷㄷㄷㄷㅐ박이었다. 그치만, 진심, 어디 있는 빌어먹을 세상에서는 `checkout --`를 파일을 되돌리는 데 쓰는 게 말이 되는거임? #LinusTorvalds에게주먹질