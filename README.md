# MyLearnAndTest_Git
study git&amp;github tutorial

## 기본 커멘드 명령어

### cd[폴더이름]:해당 디렉토리로 이동
```
cd documents  //(현재 폴더의 하위폴더인 documents 폴더로 이동)
cd /c/workspace //(절대경로 /c/workspace 로 이동)
cd..  //(상위 폴더로 이동)
```
### mkdir[폴더이름]:디렉토리 생성
```
mkdir test  //(현재 위치에 test 디렉토리 생성)
```
### touch[파일이름]:빈 파일 생성
```
touch index.txt //(현재 위치에 index.txt 파일 생성)
```
### ls 
```
ls
```
현재 디렉토리 폴더, 파일을 보여줌

## git 명령어
### 사용자 이름과 email 등록
```
git config --global user.name "[이름]"
git config --global user.email "[이메일]"
```

### git init (marster branch가 생성)
```
git init		
```
(.git 이라는 하위 폴더가 생김 건드리지 말것)

### git add 
```
 git add .	
```
(add뒤에 .은 현재 새로 만들어진 모든 파일을 대상으로 지정한다는 뜻)
(원하면 .대신에 윈하는 파일명을 입력)

### git status
```
git status  //(파일의 상태를 확인)
git status -s //(status를 간단하게 보여준다. --short로 사용 가능)
```
#### 파일의 상태
- Tracked = changes to be committed	(파일 이름이 초록색으로 보이며 add를 한 상태 커밋 가능)
- Untracked = changes not staged for commit (파일 이름 붉은색 아직 add를 하지 않은 상태)

### git commit
```
git commit
git commit -m "[커밋 이름]"
```
* 위 두 코드는 stage에 올라간 파일을 커밋
```- git commit``` 으로 커밋시 Vim편집기로 들어간다 insert로 쓰기 모드에 들어가면 가장 윗 줄에 커밋 메시지를 작성할 수 있고 ESC로 나와서 :wq, :w + :q, (오류시) :!w + :q로 종료한다.
-:wq! // 강제 저장 후 종료

-m은 커밋 메시지를 바로 작성
```
git commit -a //(unstaged 된 파일을 자동으로 staged시켜주고 커밋한다.)
git commit -am //으로도 사용 가능
```

### git rm
```
git rm [파일] //(파일을 삭제한다.)
```
- 삭제된 파일은 staged 상태가 된다.
- 커밋을 하면 파일은 삭제 되고 Git은 더이상 파일을 추적하지 않는다.

### git log
```
git log //(커밋 히스토리를 조회한다.)

git log -p  //(git diff결과를 보여준다.)
git log -patch

git log --stat  //(각 커밋의 통계 정보를 조회한다.)

git log --pretty  //(히스토리 내용을 본때 다양한 형식으로 바꿔 볼 수 있다.)
```
***그 외에 다양한게 많으니 나중에 필요하면 추가

### git commit --amend
```
git commit --amend  //(가장 최근 커밋에 현재 stage를 덮어쓴다.)
```

### git reset HEAD [file]
```
git reset HEAD [파일 이름]	(stge된 파일을 Unstage로 변경한다.)
```
### git checkout --[file[
```
git checkout --[파일 이름]	(파일의 변경사항<modified>를 이전으로 되돌린다.)
```
 ***사용에 주의!!!

