# 개념

`CAPTCHA`란 사람과 컴퓨터를 구별하기 위한 기술이며, 웹 사이트 회원가입이나 게시판 게시글 작성, 패스워드 변경 등에 사용된다. </br> 
이는 해커가 자동화 프로그램의 일종인 `봇`을 통해 악성행위를 반복적으로 수행하는 것을 차단하기 위해 `사람만이` 알아볼 수 있는 이미지, 오디오, 문자 등을 제시함으로써 사용자가 사람임을 확인한다. 
</br> </br> </br> </br> 

# 공격

## Low 레벨

`CAPTCHA` 입력 후 첫 번째 CAPTCHA 검증 페이지 요청 패킷 중 `POST body` 영역을 보면, `step`이라는 파라미터와 공격자가 입력한 </br> 
`password_new`, `password_conf` 파라미터가 존재한다. 그리고 랜덤한 값으로 추정되는 `g-recaptcha-response`가 존재한다.

