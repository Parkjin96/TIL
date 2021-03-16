# git config -author

커밋을 남기는 사람에 대한 정보(이메일, 이름)을 설정함.

```bash
$ git config --global user.name '이름'
$ git config --global user.email '이메일주소'
$ git config --global -l
```

* github 이메일 주소와 동일하게 지정하면, 커밋 기록이 github 계정과 연동되어 표기(예 - 잔디밭)
* 주의! 이 설정과 github 접근 권한(예 - push)과는 전혀 상관 없음
  * 윈도우 - 자격 증명 관리자
  * 맥 - 키체인 접근

