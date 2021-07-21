## passwd

  - ### 기능
    - 기본적으로 사용자의 암호를 변경하는 명령어이다.
  - ### 형식
    - passwd [option] [username]
  - ### 옵션
    - -l : 지정한 사용자의 계정을 사용할 수 없도록 잠글 수 있다.
    - -u : 지정한 잠금 상태의 사용자 계정을 잠금해제할 수 있다.
  - ### 사용 예
    - `passwd` : 사용자 암호 변경
    - `sudo passwd user01` : user01 사용자의 암호를 설정
    - `sudo passwd -l root` : root 계정을 잠금하여 사용할 수 없게 한다.
      - 주로 보안이 중요한 서버에서 root 계정은 잠그고 sudo 명령으로만 관리자 권한을 얻을 수 있도록 한다.
        - sudo 명령을 사용할 수 있는 그룹이나 사용자를 지정하는 파일은 <br>`~/sudoers`이다. 

<br>

## usermod

  - ### 기능
    - 지정한 user의 계정을 수정한다.
  - ### 형식
    - usermod [option] [group] [username]
  - ### 옵션
    - -a : Append, 추가, 이 명령은 '그룹에 추가'라는 의미이기에 항상 -G 옵션과 같이 사용.
    - -G : Group, 사용자가 추가될 그룹을 지정.
  - ### 사용 예
    - `sudo usermod -a -G sudo user01`
      - user01 사용자를 sudo 그룹에 추가한다. 
        - sudo 그룹은 `~/sudoers` 파일에 등록되어 sudo 명령어를 사용할 수 있다.

<br>

## id

  - ### 기능
    - 현재 로그인한 계정의 uid, gid를 보여준다.
    - 계정명을 입력하면 계정명에 대한 uid, gid를 보여준다. 
  - ### 형식
    - id [option] [username]
  - ### 옵션
    - -un : EUID 정보
    - -u : EUID의 UID 번호
    - -g : -EGID 정보
  - ### 사용 예
    - id -> 현재 로그인한 계정 uid, gid 출력
    - id root -> root 계정 uid, gid 출력
     
<br>

## who

  - ### 기능
    - 현재 시스템에 로그인한 사용자의 정보를 출력
  - ### 형식
    - who [option] [File | 입력값1, 2, ...]
  - ### 옵션
    - -a : 로그인 되어 있는 사용자의 모든 정보 출력
    - -H : 각 정보의 속성(NAME, LINE, TIME, IDLE, PID, COMMENT 등) 출력
    - -b : 시스템 부팅 시간 출력
    - -l : 시스템 로그인 프로세스 출력
    - -q : 로그인한 유저 수, 유저명을 전부 출력
    - -r : 활성화된 run level 출력
    - -u : 단일 who 명령과 비슷, 로그인한 유저 정보를 출력

<br>

## whoami

- ### 기능
  - 현재 로그인 한 사용자의 이름을 확인한다.
- ### 형식
  - whoami
- ### 사용 예
  - whoami
  - user01

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