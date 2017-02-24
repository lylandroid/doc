Git手册
======

    …or create a new repository on the command line

    echo "# doc" >> README.md
    git init
    git add README.md
    git commit -m "first commit"
    git remote add origin https://github.com/lylandroid/doc.git
    git push -u origin master

    …or push an existing repository from the command line

    git remote add origin https://github.com/lylandroid/doc.git
    git push -u origin master

git重置用户名和密码
-----------------
    验证：
          $git config --global user.email "lylandroid@163.com"
          $git config --global user.name "lylandroid"

    更改local级别的user.name（本地Repo中的config）
       # set user.name in local config and query.  tips: D:\test\TestUser is  a dictionary of Repo
       PS D:\test\TestUser> git config --local user.name NinputerWonder
       PS D:\test\TestUser> git config --local user.name
       NinputerWonder
    未验证：
         1.取消global
          git config --global --unset user.name
          git config --global --unset user.email
         2.设置每个项目repo的自己的user.email
           git config  user.email "lylandroid@163.com"
           git config  user.name "lylandroid"

android studio git错误
--------------------
    错误 Remote URL test failed: unable to access 'https://github.com/lylandroid/rookiemall.git/': error setting certificate verify locations:
        解决方式：git config --global http.sslverify "false" will solve the problem
        https://github.com/npm/npm/issues/1484

    错误：Push failed: Failed with error: fatal: unable to access 'https://github.com/lylandroid/rookiemall.git/': The requested URL returned error: 403
        解决方式：
        1，在项目目录下执行
            git remote add -f -t master -m  origin master https://github.com/lylandroid/rookiemall.git/,
        2，在使用android studio提交