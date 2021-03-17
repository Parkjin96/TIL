# push error

```bash
$ git push origin master
To https://github.com/edutak/first.git
 ! [rejected]        master -> master (fetch first)
 # push 실패.
error: failed to push some refs to 'https://github.com/edutak/first.git'
# 원격저장소 커밋이 로컬저장소에 없다.
hint: Updates were rejected because the remote contains work that you do
hint: not have locally. This is usually caused by another repository pushing
hint: to the same ref. 
# 원격저장소 변경사항들(remote changes - 커밋)를 먼저 통합시키는 것을 아마도 원할 것..
# 다시 push하기전에 (git pull....?)
You may want to first integrate the remote changes
hint: (e.g., 'git pull ...') before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.

```

## 해결 방법

```bash
$ git pull origin master
remote: Enumerating objects: 7, done.
remote: Counting objects: 100% (7/7), done.
remote: Compressing objects: 100% (4/4), done.
remote: Total 6 (delta 2), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (6/6), 1.30 KiB | 83.00 KiB/s, done.
From https://github.com/edutak/first
 * branch            master     -> FETCH_HEAD
   be95b13..a757b59  master     -> origin/master
Merge made by the 'recursive' strategy.
 README.md | 3 +++
 1 file changed, 3 insertions(+)
 create mode 100644 README.md
```

* 커밋 메시지를 작성하는 창이 나타난다. (vim 환경)

  * 저장하고 나가는 법 : `esc` + `:wq` 

  ![image-20210317111232059](md-images/image-20210317111232059.png)

* 원격저장소의 커밋과 로컬의 커밋을 병합하는 커밋이 발생함
* 다시 push!

```bash
$ git push origin master
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 12 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (5/5), 493 bytes | 493.00 KiB/s, done.
Total 5 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 1 local object.
To https://github.com/edutak/first.git
   a757b59..264db2a  master -> master
```

