# OSS-GIT

## 깃설정

$ git config --global user.name **

$ git config --global user.email **

$ git config --global core.autocrlf true 

$ git config --global core.safecrlf false 

$ git config --global core.editor 'code --wait' 

$ git config --global init.defaultBranch main 

## 브랜치 병합
#####병합(merge)
-두 개의 브랜치를 하나로 모으는 과정

$ git merge {병합할 브랜치 명}
$ git merge --no-ff {병합할_브랜치_명}
$ git merge --ff-only {병합할_브랜치_명}
$ git merge --squash {병합할_브랜치_명}
