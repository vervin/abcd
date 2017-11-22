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

第一次修改 -> git add -> 第二次修改 -> git add -> git commit

git checkout -- readme.txt

git reset HEAD readme.txt

//删除文件

rm test.txt

git rm test.txt

git commit -m "remove test.txt"

//git checkout -- test.txt

//创建一个github仓库
第1步：创建SSH Key。在用户主目录下，看看有没有.ssh目录，如果有，再看看这个目录下有没有id_rsa和id_rsa.pub这两个文件，如果已经有了，可直接跳到下一步。如果没有，打开Shell（Windows下打开Git Bash），创建SSH Key：

$ ssh-keygen -t rsa -C "youremail@example.com"
你需要把邮件地址换成你自己的邮件地址，然后一路回车，使用默认值即可，由于这个Key也不是用于军事目的，所以也无需设置密码。

如果一切顺利的话，可以在用户主目录里找到.ssh目录，里面有id_rsa和id_rsa.pub两个文件，这两个就是SSH Key的秘钥对，id_rsa是私钥，不能泄露出去，id_rsa.pub是公钥，可以放心地告诉任何人。

第2步：登陆GitHub，打开“Account settings”，“SSH Keys”页面：

然后，点“Add SSH Key”，填上任意Title，在Key文本框里粘贴id_rsa.pub文件的内容

//上传到github
git remote add origin git@github.com:vervin/abcd.git
push -u origin master

