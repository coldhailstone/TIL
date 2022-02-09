## git 전역 사용자 설정
    $ git config --global user.name "John Doe"
    $ git config --global user.email johndoe@example.com

## 주요 명령어
    $ git init
        > 저장소 초기화
        > .git 폴더 생성
    $ git remote add <단축이름> <url>
        > 원격 저장소 추가
    $ git clone <url>
        > 다른 원격 저장소 복제
    $ git status
        > 파일의 상태 확인
    $ git add <file>
        > 해당 파일 추적
    $ git commit -m <message>
        > 로컬 저장소 변동사항 저장
        > --amend
            >> 마지막 커밋에 덮어씌우기
    $ git push <remote> <branch>
        > 커밋된 내용을 원격 저장소로 내보냄
    $ git pull
        > 원격 저장소에서 로컬 저장소로 소스를 가져옴
    $ git branch <branchname>
        > 커밋 사이를 이동할 수 있는 포인터 같은 것
        > 독립적인 작업 공간
    $ git merge
        > 여러 브랜치를 단일 브랜치로 병합
    $ git stash
        > 작업 중 브랜치를 이동해야 할 경우 기존 작업 임시 보관
    $ git reset --hard <commit_id>
        > 커밋을 취소
        > 원하는 커밋으로 HEAD 이동
        > 이력을 남기지 않음
    $ git revert <commit_id>
        > 원하는 커밋으로 돌아감
        > 이력을 남김
    $ git cherry-pick <commit_id>
        > 다른 브랜치의 커밋 불러오기
