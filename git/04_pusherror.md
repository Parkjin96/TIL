# push error

```bash
$ git push origin master
To https://github.com/edutak/first.git
 ! [rejected]        master -> master (fetch first)
 # push 실패.
 
error: failed to push some refs to 'https://github.com/edutak/first.git'
# 원격 저장소 커밋이 작업이 로컬 저장소에 없다.
hint: Updates were rejected because the remote contains work that you do
hint: not have locally. This is usually caused by another repository pushing
hint: to the same ref.
# 원격 저장소 변경사항들(remote changes - 커밋)를 먼저 통합시키는 것을 아마도 원할 것..
# 다시 push하기 전에 (예 git pull...)
You may want to first integrate the remote changes
hint: (e.g., 'git pull ...') before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.

```

## 해결방법

```bash
$ git pull origin master
```

* 커밋 메세지를 작성하는 창이 나타난다.(vim환경)
  * 저장하고 나가는 법 : `esc` + `:wq`
* 원격 저장소의 커밋과 로컬의 커밋을 병합하는 커밋이 발생함.
* 다시 push