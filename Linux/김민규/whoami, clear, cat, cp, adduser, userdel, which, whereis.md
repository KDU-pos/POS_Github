## whoami

- ### 기능
  - 현재 로그인 한 사용자의 이름을 확인한다.
- ### 형식
  - whoami
- ### 사용 예
  - whoami
  - user01

<br>

## clear

- ### 기능
  - 현재 쉘의 화면을 청소한다.
  - 로그가 지저분하게 쌓였을 때 가시성을 위해 사용한다.
- ### 형식
  - clear
- ### 사용 예
  - clear
  - ctrl + L

<br>

## cat

- ### 기능
  - 지정한 파일의 내용을 텍스트로 출력한다. 
- ### 형식
  - cat [option] [file]
- ### 사용 예
  - cat text01
  - cd /bin -> cat ls

<br>

## cp

- ### 기능
  - 파일이나 디렉터리를 복사
  - 파일이나 디렉터리를 백업할 때 활용 가능하다.
- ### 형식
  - cp [Option] [File(Directory)] [File2(Directory)]
  - 왼쪽의 파일을 오른쪽으로 복사
  - 옵션이 없으면 파일만 복사할 수 있다.
- ### 옵션
  - -i : 파일2가 존재하면 덮어쓸 것인지 물어본다.
  - -r : 디렉터리를 복사할 때 지정한다. 이때 디렉터리 하위파일과 디렉터리까지 복사된다.
- ### 사용 예
  - cp dir/test.txt dir2/
    - dir 하위의 test.txt 파일을 dir2 디렉터리에 복사
  - cp -r dir dir2
    - dir 디렉터리를 dir2 디렉터리에 복사
    - dir 디렉터리는 dir2의 하위 디렉터리가 된다.
  - cd /bin -> cp ls backupfile -> rm ls -> cp backupfile ls 
    - /bin 디렉터리의 ls 명령어 파일을 backupfile 파일에 복사한다. 
      - backupfile 파일은 /bin 디렉터리에서 존재하지 않으면 자동으로 생성된다. 
    - /bin 디렉터리의 ls 명령어 파일을 삭제한다.
      - ls 명령어를 사용할 수 없지만, backupfile 파일을 명령어로 사용하여 기존 ls의 기능을 사용할 수 있다. 
    - /bin 디렉터리의 backupfile 파일을 ls 파일에 복사한다.
      - backupfile에 백업해 두었던 ls 파일 데이터를 다시 ls 파일에 복사한다. 
      - ls의 기능을 하는 파일이 두 개 존재하게 되었다. 

<br>

## adduser 

 - ### 기능
   - 유저를 생성한다.
   - 생성 시 유저의 홈 디렉터리를 자동으로 지정해준다.
   - 생성 시 해당 유저의 실제 이름과 전화번호, 직장 정보 등을 입력할 수 있다.
 - ### 형식
   - adduser [option] [username]
 - ### 사용 예
   - adduser kims

<br>

## userdel

  - ### 기능
    - 유저를 삭제한다.
  - ### 형식
    - userdel [option] [username]
  - ### 옵션
    - 없음 : 유저의 계정 정보만 삭제되고 홈 디렉터리와 메일 파일은 그대로 존재
    - -r : 유저의 계정 및 홈 폴더 등 유저와 관련된 모든 파일 삭제
  - ### 사용 예
    - userdel -r user01

<br>

## which

  - ### 기능
    - 특정 명령어의 위치만을 찾아주는 명령어이다.
    - 경로를 절대 경로로 출력한다.
  - ### 형식
    - which [option] [command]
  - ### 옵션
    - -a : 'all', 검색 가능한 모든 경로에서 해당 명령어를 찾음.
  - ### 사용 예
    - which -a ls -> /usr/bin/ls, /bin/ls
      - ls 명령어 파일이 있는 모든 경로를 출력

<br>

## whereis

  - ### 기능
    - 명령어의 실행파일 위치, 소스 위치, man 페이지 파일의 위치를 찾아주는 명령어이다.
  - ### 형식
    - whereis [option] [command]
  - ### 사용 예
    - whereis ls -> ls: /usr/bin/ls /usr/share/man/man1/ls.1.gz
