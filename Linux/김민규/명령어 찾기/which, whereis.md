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
