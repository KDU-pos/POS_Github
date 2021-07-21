## chown

  - ### 기능
    - 디렉토리 또는 파일의 소유자를 변경한다.
  - ### 형식
    - chown [user:group] [filename | directory]
  - ### 사용 예
    - 파일 소유자만 변경
      - `-rw-r--r-- user01  group01  a.txt` -> <br>`chown user02: a.txt` -> <br> `-rw-r--r-- user02  group01  a.txt`
    - 파일 소유 그룹만 변경
      - `-rw-r--r-- user01  group01  a.txt` -> <br>`chown :group02 a.txt` -> <br> `-rw-r--r-- user01  group02  a.txt`
    - 파일 소유자와 그룹 모두 변경
      - `-rw-r--r-- user01  group01  a.txt` -> <br>`chown user02:group02 a.txt` -> <br> `-rw-r--r-- user02  group02  a.txt`
    - 디렉터리 소유자와 그룹 모두 변경
      - `drw-r--r-- usr01  grp01  /home/test` -> <br>`chown usr02:grp02 /home/test` -> <br> `drw-r--r-- usr02  grp02  /home/test`