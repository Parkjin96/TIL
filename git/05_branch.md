# branch

## 기본 명령어

* branch 생성

  ```bash
  $ git branch __브랜치이름__
  ```

* branch 이동

  ```bash
  $ git checkout __브랜치이름__
  Switched to branch 'ppt'
  ```

* branch 생성 및 이동

  ```bash
  $ git checkout -b __브랜치이름__
  ```

* branch 병합

  ```bash
  (master) $ git merge __브랜치이름__
  ```

  * `master` 브랜치에 `__브랜치이름__` 을 병합

* branch 목록

  ```bash
  $ git branch
  * master
    ppt
  ```

* branch 삭제

  ```bash
  $ git branch -d __브랜치이름__
  Deleted branch ppt (was ff03b20).
  ```

  