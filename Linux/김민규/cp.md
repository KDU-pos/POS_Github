## cp

- ### 기능
  - 파일이나 디렉터리를 복사
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