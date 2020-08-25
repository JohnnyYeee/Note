#GIT (-h to show help menu)
课程里常用的命令行总结
Some useful commands which will be used during our course

Windows用户请尽量使用Git bash，不过大部分情况下powershell也可以，请自己尝试。



1. 打印出当前所在的目录directory


```
$ pwd
/Users/pengxiao
```

2. 打印出当前所在folder里的所有的文件和文件夹


```
$ ls
Applications       Downloads          Library            Pictures           VirtualBox         mongodb       
Desktop            Dropbox            Movies             Public             git-test           opt                tmp
Documents          GNS3               Music              PycharmProjects    jupyter-demo       python-demo        vagrant
```
我们可以使用 `ls -l` to print all the files and directories with types and other information

通过-l可以列出文件和文件夹的一些属性

`ls -la` 

```
$ ls -l
total 0
drwx------@  5 pengxiao  staff   160 Dec  1  2018 Applications
drwx------@ 10 pengxiao  staff   320 Apr 26 13:02 Desktop
drwx------@ 20 pengxiao  staff   640 Apr 24 10:57 Documents
drwx------@ 27 pengxiao  staff   864 Apr 26 13:16 Downloads
-rw-r--r--   1 pengxiao  staff     0 Apr 26 13:30 test.txt
drwxr-xr-x  15 pengxiao  staff   480 Apr 20 23:20 tmp
if the output starts with d, that means it is a directory if starts with -, means file
```
以d开头的是文件夹，以-开头的是文件



below is a directory

`drwxr-xr-x  15 pengxiao  staff   480 Apr 20 23:20 tmp
`
and below is a file

`-rw-r--r--   1 pengxiao  staff     0 Apr 26 13:30 test.txt
`

3. change the current working directory改变当前的工作目录

From the ls output above, there is a directory called tmp

we can use cd command to go inside of the tmp directory

```
$ cd tmp
$  pwd
/Users/pengxiao/tmp
```
we can use cd .. to go to the parent directory 可以到上一层目录

```
$ pwd
/Users/pengxiao/tmp
$ cd ..
$ pwd
/Users/pengxiao
$
```


#github instruction basic local
`find .git` find main catalog

`vim .git/config` way to change the create info

`git status` check status

`git log` see the log

```
echo "# test2" >> README.md
git init
git add README.md
git commit -m "first commit"
git remote add origin https://github.com/JohnnyYeee/test2.git
git push -u origin master
```

#REMOTE
##branch and merge

`git branch` show current branch

`git branch branch_name ` add new branch with the new name

`git checkout` show current branch

`git checkout -b new_branch_name` create and switch to new branch 

`git checkout branch_name` switch to another branch

`git diff another_branch_name` see the diff of branches

`git merge another_branch_name` merge another branch by adding the diffs

#ftech and pull
`git remote -v`  show current version of repository on github

`git fetch orgin master` cp current version of repository on github

fetch_head in .git contain the newest commit num github

head in .git contain the current commit num in the computer

`git diff FETCH_HEAD` see the diif between local and gihub

`git merge FETCH_HEAD` UPDATE THE THE NEWEST VERSION ON GITHUB

cd .. return to main folder

`git pull` directly copy the new version from github to local (two step in one)

`git push origin test`  push the new branch "test" to the github

#delete remote branch
`git branch -a` show all branch at loacl and remote

`git push origin test` update another branch "test" to github

`git push -d origin test` delete another branch

`git branch -m test51 testy` change the branch name

#tag
 
` git tag -l` list tags at local

`git fetch -h` ask help of git fetch

`git fetch -t` fetch all tags

`git tag New_tag_name`  create new tage of current branch and commit

`git push --tag`  push local tags to github

`git tag -d v1.0` delete local tag "v1.0"

`git push origin :refs/tags/V1.1` delete tags on github



#git
```
$ git config --global user.name "Your Name"

$ git config --global user.email "your email address"
```

`git ls-files -s` show the files on staging area

`git rm --cached test.txt` remove the files record in staging area

`git restore --staged file1.txt` restore the staging record to the previous one

`git restore file1.txt` restore the file to the previous one

`git cat-file -t hash_num` see the meaning og hash_num

`git cat-file -p hash_num` see the property 

`cat` read files and show the output

`tree "pwd"` show structure

`git log --oneline` show log (simple version)

`git shortlog` short log

`git. log --help`


  ![](https://github.com/JohnnyYeee/git_test/blob/master/note1.png?raw=true)
  
  ![](https://github.com/JohnnyYeee/git_test/blob/master/note2.png?raw=true)
  
  
  `git reflog` see the history log
  
 `git diff --cached`compare the staging area and the github
 
 `git restore`  and `git checkout` to restore file
 
 `git reset ORIG_HEAD` 回撤到之前的一次commit
 
`git rebase master` move another branch to the top of master

`git push ....... --force ` after rebase need "--force" to push the branch


![](https://github.com/JohnnyYeee/Photohub/blob/master/git/git%20basic.png?raw=true)

![](https://github.com/JohnnyYeee/Photohub/blob/master/git/git%20branch.png?raw=true)

![](https://github.com/JohnnyYeee/Photohub/blob/master/git/git%20remote.png?raw=true)



`git remote show origin` show the remote info

`git reset --hard ORTIG_HEAD` 硬回滚


`git cat-file -t .....` 显示文件类型

`git cat-file -p .....` 显示文件内容

`du -h .git/objects` 显示文件大小

`git gc` 压缩

`git fsck` show the trash objects

`git prune` remove the trash object

·git cherry-pick· similar to merge

#gitignore
create ".gitignore"   incclude `*.out` to ignore .out file


`git commit --amend` change the last commit


#git reset
![](https://github.com/JohnnyYeee/Photohub/blob/master/git/git%20reset%203%20way.png?raw=true)

#git tag

![](https://github.com/JohnnyYeee/Photohub/blob/master/git/git%20tag.png?raw=true)

![](https://github.com/JohnnyYeee/Photohub/blob/master/git/tag%20operation.png?raw=true)


#gitstash
![](https://github.com/JohnnyYeee/Photohub/blob/master/git/git%20stash.png?raw=true)
