---
layout: post
title: tool tricks
subtitle: --
gh-repo: daattali/beautiful-jekyll
gh-badge: [star, fork, follow]
tags: [daily tricks]
comments: true

---
##1 BFG tool to simplify .git repo
#### download page

>https://rtyley.github.io/bfg-repo-cleaner/

#### usage:

>java -jar bfg-1.14.0.jar -b 2M mmagnn/.git

#### if protected commits append the command

>--no-blob-protection

>java -jar bfg-1.14.0.jar -b 2M mmagnn/.git --no-blob-protection

##2 git large file manage

~~~
>查找大于50M的文件
 find . -type f -size +50M
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

##3 jupyter_config
jupyter_personal_config: 

### work with conda envs：
   1) install nb_conda_kernels in the base env : 
   >conda install nb_conda_kernels
   
   2) install ipykernel in needed env: 
   >conda install ipykernel
   
### remove env:
  >jupyter kernelspec remove env_name

##4 conda
导出环境
>conda env export > env.yml

导入环境
>conda env create -f env.yml



*[HTML]: HyperText Markup Language
*[CSS]: Cascading Style Sheets
*[JS]: JavaScript