$ git config --global user.name "Your Name"
$ git config --global user.email "email@example.com"
$ mkdir learngit
$ cd learngit
$ pwd

$ git init

//创建一个文件readme.txt

git status

git add readme.txt

git status

git commit -m "first commit"

//更改readme.txt

git status

git diff readme.txt

git add readme.txt

git commit -m "second commit"

要随时掌握工作区的状态，使用git status命令。

如果git status告诉你有文件被修改过，用git diff可以查看修改内容。


git log

git log --pretty=oneline

git reset --hard HEAD^

cat readme.txt

git reset --hard 3628164

git reflog  //历史
