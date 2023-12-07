# OSS-GIT

## 깃설정

$ git config --global user.name **

$ git config --global user.email **

$ git config --global core.autocrlf true 

$ git config --global core.safecrlf false 

$ git config --global core.editor 'code --wait' 

$ git config --global init.defaultBranch main 

## 브랜치 병합
##### 병합(merge)
-두 개의 브랜치를 하나로 모으는 과정

###### -$ git merge {병합할 브랜치 명}
###### -$ git merge --no-ff {병합할_브랜치_명}
###### -$ git merge --ff-only {병합할_브랜치_명}
###### -$ git merge --squash {병합할_브랜치_명}

## 병합취소
-취소
###### -$ git merge --abort$ git merge --abort
-다시 병합
###### $ git merge feat/list
-추가, 커밋 다시
###### $ git commit –am 'Resolve conflict, main'

-3-way 충돌 발생
###### $ git merge hotfix
-충돌한 파일을 인지하고 파일 수정
###### $ code file
-수정 후 다시 add, commit
###### $ git commit –am ‘msg’
-충돌 이후 병합 취소
###### $ git merge --abor
