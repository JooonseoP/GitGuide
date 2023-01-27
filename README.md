# Git 사용방법 정리
Git의 설치 방법과 사용방법, 또 자주쓰는 명령어 들을 정리하여 본다.

## Git 설치
참고 : https://code-lab1.tistory.com/249

1) 다운로드  
![다운로드 이미지](https://blog.kakaocdn.net/dn/bau3CO/btrHxM7OYJN/r6EzlPwWbCsdIvddYZGSB0/img.png)  
다음의 링크에 들어가 자신의 컴퓨터 환경(Window, 보통 윈도우 10이라면 64bit)에 맞는 Git을 다운 받는다.   
git : https://git-scm.com/downloads

2) 설치 진행  
다운로드 받은 설치 파일을 실행하여 진행한다.  
1)) 첫 페이지는 라이센스관련 Next를 누른다.  
![설치 이미지1](https://blog.kakaocdn.net/dn/bcbyN0/btrHxMfIf5q/nxkfi2TxhKETQdJznF0sE0/img.png)  
2)) 두번 째 페이지는 설치 경로 설정. 설치 경로는 보통 C:\Program Files\Git에 두는 데 원하는 경로가 따로 있으면 따로 설정하고, Next를 눌러 진행한다.  
![설치 이미지2](https://blog.kakaocdn.net/dn/bjezCJ/btrHDPIXpfu/xMakyUlA5GwbHjeFNZZKUk/img.png)  
3)) 여러가지 설정을 하는 창, 보통 그대로 설치하면 되는 데 다음 과 같은 옵션을 정리한다.  
![설치 이미지3](https://blog.kakaocdn.net/dn/F9zDE/btrHDdjikV8/Gc5wWvEm6QTKbHTbMvUK0k/img.png)  
- Additional icons > On the Desktop : 바탕화면에 아이콘 추가
- Windows Explorer integration
- Git Bash here : Git Bash 연결 기능 (폴더에서 Git을 바로 연결할 수 있는 기능)
- Git GUI here : Git GUI 연결 기능
- Git LFS(Large File Support) : 용량이 큰 파일 지원
- Associate .git* configuration files with the default text editor : git 구성 파일을 기본 텍스트 편집기와 연결
- Associate .sh files to be run with Bash : .sh 파일을 Bash와 연결
- Check daily for Git for Windows updates : 윈도우 용 Git 업데이트를 매일 확인할 것인지
- (NEW!) Add a Git Bash Profile to Windows Terminal : Bash 프로필을 윈도우 터미널에 추가할 것인지  
4)) 시작폴더 경로를 선택하는 창이 나온다. 'Don't create State Menu folder'를 선택하면 시작메뉴에 추가하지 않는다. 일반적으로는 아무것도 건드리지 않고, Next를 눌러 다음으로 넘어간다.   
![설치 이미지4](https://blog.kakaocdn.net/dn/dXJ3CB/btrHAvSgnC3/yIzkbFBKZr4YUndfLFExkK/img.png)   
5)) Git을 사용할 기본 에디터를 선택하는 창. 기본 에디터로 Vim 되어 있으나, 사용해본 Tool이 있다면, 원하는 기본 에디터를 설정하도록한다.  
![설치 이미지5](https://blog.kakaocdn.net/dn/3hZfx/btrHCW27jJp/1LNPuph9f81AkoF70pqpU0/img.png)  
6)) 브랜치 개념을 알야한다. 'git init' 이라는 명령어를 사용한 직 후에 기본 branch 이름을 뭐라고 설정할 것인지 선택하는 창이다. 'Let Git decide'는 깃의 기본 브랜치 이름(master)를 사용하겠다는 것이고, 두번째 선택지는 브랜치 명을 직접 선택하는 것이다. 우선 기본인 'Let Git decide'를 선택한다.  
![설치 이미지6](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FbM8YF6%2FbtrHtgIkMSi%2F5mLB9P8a88sczskdkbYdPK%2Fimg.png)  
7)) 환경변수 옵션을 설정하는 창이다. 두번째 선택지를 골라서 Bash외에서도 Git을 활용할 수 있게 하자.  
![설치 이미지7](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FdcRaFf%2FbtrHDzM9pgH%2Fdos8hWnz29bglxSB0hekRk%2Fimg.png)  
8)) SSH실행 도구를 선택하는 창, 첫번째를 선택하고 다음으로 넘어간다.  
![설치 이미지8](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FbnGUGr%2FbtrHEzMF8CD%2F138DSSvqrrkphvrW7B9ock%2Fimg.png)  
9)) HTTP 연결 옵션을 선택하는 창. 첫 번째는 OpenSSL 라이브러리를 사용한다는 뜻이고 두 번째는 윈도우 인증서 저장소를 사용하여 검증한다는 뜻이다. 첫 번째를 선택하자.  
![설치 이미지9](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2Fb4aXZo%2FbtrHDjwOXtk%2F7TBLSlz3O08UsURkSRaC7K%2Fimg.png)  
10)) 개행 스타일을 선택하는 창. 개행이라는 것은 줄 바꿈을 의미한다. 크로스-플랫폼 프로젝트를 위해 첫번째 선택지를 고르는 걸 추천한다.  
![설치 이미지10](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FkYBed%2FbtrHEehGmpD%2FV29mRpStttjgvkaKz5rtCk%2Fimg.png)  
11)) Git Bash 터미널 에뮬레이터를 설정하는 창. 첫 번째는 기본 터미널 에뮬레이터, 두 번째는 윈도우 기본 콘솔(CMD)이다. 첫 번째를 선택하자.  
![설치 이미지11](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FMW67F%2FbtrHDA6mjAt%2Fa7EdZjVkDI1YkxYP6lZkw0%2Fimg.png)  
12)) "git pull" 명령어에 수행될 작업을 선택하는 창. "Default(fast-forward or merge) : 기본 동작을 실행한다." 첫 번째를 선택하자.  
![설치 이미지12](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FbtOEYy%2FbtrHzpFeQLs%2FdyOKY0U2OkZJClHPdSzIE0%2Fimg.png)  
13)) 자격 증명 도우미를 선택하는 창. 첫 번째는 기본 자격 증명 도우미를 사용하는 것이고 두 번째는 사용하지 않는 것이다. 첫 번째를 선택하자.  
![설치 이미지13](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FbsQ3y6%2FbtrHEeBY9es%2FKJqfqDBYfUNaFG8y7e1Um1%2Fimg.png)   
14)) 추가 옵션을 선택하는 창. 첫 번째는 파일 시스템 캐싱 기능을 사용해 성능을 높이는 옵션이므로 꼭 선택해주자. 두 번째는 심볼릭 링크를 활성화하는 것이다. 첫번째만 선택하고 넘어가자.  
![설치 이미지14](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2Fc0oy8g%2FbtrHCn7MRlw%2FZYfK5w1GuqewDGkJHE0l6K%2Fimg.png)     
15)) 실험적인 기능을 사용할 것인지 묻는 창. 첫번째는 winpty를 사용하지 않고 Bash에서 Node나 Python 같은 콘솔을 실행할 수 있게 한다. 하지만 버그가 존재한다. 두번째는 명령어 실행 속도를 높이기 위해 built-in file system monitor를 자동으로 실행하는 것이다. 혹시 모를 버그를 방지하려고 나는 둘 다 선택하지 않았다.  마지막으로 Install을 누르면 설치가 진행된다.  
![설치 이미지15](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FKvD7V%2FbtrHDcSeeq7%2FzVQ9JJRgyTjTOYPz3zzupK%2Fimg.png)  
16)) 설치가 완료되었다. 제대로 설치됐는지 확인해본다. 'Launch Git Bash'를 체크하고 Finish를 눌러 Git Bash를 실행한다.  
![설치 이미지16](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FdEWyI3%2FbtrHBBrFsxc%2FpEOkqm2EuEumsNVVJztKKk%2Fimg.png)  
  
1) 설치 확인 및 사용자 등록  
  
1))  
```c
git config --global user.name "사용자이름"
git config --global user.email "사용자이메일@...com"
```
위와 같이 입력하여 사용할 이름과 이메일을 등록한다. 이 이름과 이메일은 Git을 사용하는 사용자에 대한 등록으로 GitLab에서 등록한 이름과 이메일과는 크게 상관없다.  
```c
git config --list
```
위와 같이 입력하면 등록이 되어있는지 확인할 수 있다.  
  

### Git의 원리
(참고 : https://shxrecord.tistory.com/179)  
  
![Git의 원리 설명 이미지](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FcJ9IZ5%2FbtqDY1lY72w%2FZbMyGb6E3M412A9ordJDs1%2Fimg.png)  
Git은 위와 같이 사용되는데 작업 공간에서 작업하던 프로젝트를 작업자 PC의 가상공간인 준비영역에 저장한다. 이를 'add'라고 한다. 그렇게 더해진 준비 영역의 데이터를 로컬 저장소에 저장하기 위해서 약간의 설명을 적고 원격 저장소에 저장하기를 준비한다. 이 과정이 'commit' 준비가 다 된 Commit으로 포장된 내용을 Push를 통해 원격 저장소, Git이라 불리는 저장소에 정보를 올리게 된다.  
즉 임시공간에 저장한 내용이나 commit 까지 한 내용이 전부 올라가는 것이 아니라 push를 하기 전까지는 git에 올라가지 않는다. 하지만 그 사이의 잘못된 부분이 있으면 수정이 어렵기 때문에 한사람의 프로젝트 뿐만 아닌 여러 사람이 같이 작업중이 프로젝트를 다룰수도 있는 부분이기에 사용에는 조심해서 정보를 업데이트, 커밋해주도록한다.  
  
<용어설명>  
- 작업 공간: 올리고자 하는 파일이 있는 곳. 이 공간에 Git을 생성하여 형상 관리를 하게된다.  
- 준비 영역 : add를 통해 작업공간에 파일들이 저장된다. 로컬 저장소에 commit 되기 전 거쳐가는 영역이지만 준비영역을 거치지 않고 commit도 커밋이 가능하다.  
- 로컬 저장소 : 준비 영역에 있던 파일들을 commit하게 되면 로컬 저장소에 저장되며 최종 버젼이다.  
- 원격 저장소 : 로컬 저장소의 파일들이 push를 통해 원격 저장소에 올라간다.  

#### Git 파일 업로드(Commit) 방법
   
*Git의 가장 기본이 본래 master 였으나 2022년 7월 경 main으로 변경하였다. 노예제를 연상캐한다고 바뀌게 된 내용으로  
전에 master로 올리니 전부 Branch 취급되어 내용이 업데이트 되었던 부분이 있어 그 부분을 수정하였다. 다만 일부 버젼에서 오류가 
발견되었고, 현재 우선 여기의 가이드에서는 master로 작성해둔다.  
  
1) 올리고자 하는 폴더에서 마우스 우측을 눌러 Git Bash Here를 클릭한다.  
![Git 사용방법1](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FzUY7g%2FbtqDWsLmU27%2F85XiM8LvBsbhQJDBuUT4QK%2Fimg.png)  
이러지 않고선 Git Bash를 따로 실행하여 cd로 원하는 위치로 실행하는 것인데, 마우스 우측을 눌러 직접 폴더에 접속 하는 편이 편하다.)  

2) 다음을 작성하여, 현재 폴더를 로컬 저장소로 지정한다.  
```c
git init
```
다음이 정상작동하면 Bash를 클릭한 폴더 아래 '.git'이라는 파일이 생성된다.  
![Git 사용방법1_1](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2Fb5HJfG%2FbtqDURrO6JU%2FPfGGjZZLpszbDGIp7R8bp0%2Fimg.png)  

3) 다음을 작성하여, 상태를 확인한다.  
```c
git status
```
현재 Git의 상태를 보여주는 것으로 add로 가상공간이나 웹에 올락지 않은 부분은 폴더나 수정된 파일이 있는 빨간색 폰트로 나오게 되고, Git에 이미 저장되있거나, 저장되어있지만 하얀색으로 나온다.  

4) 가상공간에 파일들을 저장한다.  
```c
git add . 
``` 

위를 작성하여 저장소에 저장되지 않은 모든 폴더들을 저장한다.  
git add '폴더명'으로 원하는 폴더만 선택하여 올릴 수 도 있다.  

5) 메시지 저장 commit  
```c
git commit -m '메시지'
```
add로 저장된 폴더들에 대하여 간단한 comment를 '메시지' 부분에 추가할 수 있다.  

6) 로컬 저장소와 원격저장소를 연결시킨다.  
```c
git remote add origin '대상 주소'
``` 
가상공간에 저장된 내용을 해당 Git에 올리기 위해 주소로 된 곳과 연결을 시켜주어어야 한다.  

해당 명령을 한 뒤  

```c
git remote -v
```
를 입력하여 현재 저장된 곳이 어딘지를 확인할 수 있다.  

7) 저장한 파일들을 원격 저장소로 올린다.  
```c
git push origin master
```
위를 실행하면 원하는 git에 파일이 업로드 된다.  

업로드 된 파일은 바로 올라가진 않고 약 30초 정도 있다가 올라간 것을 확인해볼 수 있다.  

##### Git 파일 최신화 (Update) 방법
Git은 여러 사람이 공동된 작업을 할 때 한 프로젝트를 공유하여 나눌 수 있다. 이 때 내 자신이 작업한 부분과 남이 작업한 부분이 달라 다른 사람이 작업한 부분을 업데이트 받고 싶을 때가 있다.  
  
이부분은 원하는 폴더(해당 폴더 안에 'git init'이 되어 있고 원격주소와 연결이 되어있다는 전제하에) 안에서 Git Bash를 통하여 들어가고   
  
```c
git Pull origin master
```
  
를 통하여 받을 수 있다.  
  
단 다른 사람이 작업한 내역을 받는 것이기 떄문에 본인이 작업한 부분이 분실되거나 변경될 수 있다. 이 점을 조심하여 조심해서 업데이트 받도록하자.  
  
그래서 이를 방지하기 위해서 Branch란 개념이 있다.  
  
###### Git Branch 
(참고 : https://kotlinworld.com/273)  
  
Branch란 가지란 뜻으로 한가지의 프로젝트를 한 가지에서 여러가지로 뻗어나가는 가지처럼 한프로젝트를 여러방향으로 제작하거나 업무를 나눠 제작할 때 부분 적으로 나눠 제작하는 방법이다.  
  
즉 한 Git에 여러가지 버젼을 제작해서 업로드 할 수 있다는 것인데  
  
다양한 사람들과 작업하는 데나 한 프로젝트가 여러 버젼을 가져야 되는 상황이 있다면 유리하다.  
  
1) branch 생성하기  
  
원하는 폴더를 오른쪽으로 클릭하여 'Git Bash'를 눌러 들어간다.  
  
해당 폴더가 git에 연결이 되어 있는 프로젝트면 다음을 바로 실행하나  
  
되어 있지 않다면, branch를 만들 고 싶은 대상의 원격 주소에 접속하여 있어야한다.  
  
(git remote add origin '원격주소' 를 이용하여 해당 주소로 접속한다.)  
  
```c
git branch '브랜치 이름'
```
  
그런 다음 접속해 있는 원격의 위치에서 만들어준 주소로 옮길 필요가 있다.  
  
```c
git switch '브랜치 이름'
```
  
를 작성하여 위치를 바꿔준다. 만일 만들면서 바로 이동하고 싶다면  
  
```c
git checkout -b '브랜치 이름'
```
를 작성하여 만들고 바로 이동한다.  
  
이동이 되었다면 확인으로  
  
한번더 git switch '브랜치 이름'를 작성하여  확인하거나, git remote -v 를 작성하여 현재 연결되어 있는 주소를 확인한다.  
  
2) branch로 파일 업로드 하기  
위의 내용이 완전하게 확인디 되었다면 다음을 작성하여 파일을 업로드 해준다.  
  
```c
git push origin '브랜치 이름'

``` 
  
업로드 된 파일은 Git에서 확인할 수 있다.  
  
3)Git Merge  
프로젝트가 다 따로 나눠진 다음 하나로 합쳐서 하나의 프로젝트를 만들어야 되는 순간이 있다.  
그럴때 사용하는 것이 Merge다, Merge의 사용법을 알아보자.  
(참고 : https://goddaehee.tistory.com/275)  
  
Branch를 올리는 것과 비슷하나 메인(master)으로 이동한다.   
  
```c
git switch master
```
  
혹은  
  
```c
git checkout master
```
  
을 사용해 master로 이동한다.  
  
```c
git merge '합병할 브랜치 이름'
```
  
별다른 문제가 없다면 두 프로젝트가 이상없이 합쳐질 것이다.  
  
but, 두 파일의 합쳐지는데 이상이 발생한다면. 'CONFLICT'가 발생한다. 주로 파일명 의 오류나 
폴더 안에 존재하는 파일을 다른 폴더로 옮겼다는 이유로 발생한다. 해결할 수 있는 문제라면 
해당 문제를 해결해주고 와서 다시 Merge를 시도한다.  
  
만일 이리저리 해결이 안된다고하면,  
  
```c
git merge --adbort
```
  
를 작성하여 진행중인 merge를 해제하고 시도 전으로 이동할 수 있다.  

