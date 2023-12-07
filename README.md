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

## rebase 방법
-topic에서 main을 rebase 한 이후, 다시 main으로 이동 fast-forward 병합 수행
###### $ git checkout topic
###### $ git rebase main
###### $ git checkout main
###### $ git merge topic

## 최근 커밋 메시지 수정
-기본 편집기 설정 방법
###### $ git config --global core.editor ‘code --wait’
-설정된 편집기로 최근 커밋 메시지 수정
###### $ git commit --amend
-최신 4개를 부분 메시지 수정
###### $ git rebase --interactive HEAD~4

-주요 rebase –i 대화형 명령어
###### p(ick): 해당 커밋을 수정하지 않고 그대로 사용
###### r(eword): 개별 커밋 메시지를 다시 작성
###### s(quash): 계속된 이후 커밋을 이전 커밋에 결합
###### d(rop): 커밋 자체를 삭제

## 되돌리기
-reset 옵션 --hard

###### $ git reset --hard HEAD~
###### $ git reset --hard HEAD~2(HEAD~2의 내용으로 작업 디렉토리와 스테이징 영역, 깃 저장소에 복사)
###### $ git reset --mixed HEAD~2(HEAD~2의 내용으로 스테이징 영역과 깃 저장소에 복사)
###### $ git reset --soft HEAD~(HEAD~2의 내용으로 깃 저장소에 복사)

##### $ git reset --옵션 commitID
###### --hard
###### 인자인 커밋 깃 저장소의 내용을 작업 폴더와 스테이지 영역, 그리고 깃 저장소 모두에 복사・수정
###### --mixed
###### 기본 옵션으로 스테이지 영역과 깃 저장소 두 곳에 복사・수정
###### --soft
###### 깃 저장소에만 복사・수정하므로 작업 폴더와 스테이지 영역은 이전 내용이 그대로 남음

