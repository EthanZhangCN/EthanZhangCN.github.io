---
layout: post
title:  "git use log"
tags:
   - dactl
   - jekyll
description: >
	git use log
hero: https://source.unsplash.com/collection/430471/
overlay: green
published: true
---

{: .lead}
<!–-break-–>
## BFG tool to simplify .git repo
#### download page

>https://rtyley.github.io/bfg-repo-cleaner/

#### usage:

>java -jar bfg-1.14.0.jar -b 2M mmagnn/.git

#### if protected commits append the command

>--no-blob-protection

~~~js
java -jar bfg-1.14.0.jar -b 2M mmagnn/.git --no-blob-protection
~~~

## git large file manage

~~~
>查找大于100M的文件
 find . -type f -size +100M
>标记为大文件管理
git lfs track "./xxx.zip"
>追踪大文件管理记录
git add .gitattributes
提交
>git commit -m "添加了大文件"
>git push 



~~~

>查看哪些是lfs管理
git lfs ls-files

# ----------

*[HTML]: HyperText Markup Language
*[CSS]: Cascading Style Sheets
*[JS]: JavaScript