---
layout: post
title:  "git use log"
# tags:
#   - dactl
#   - jekyll
hero: https://source.unsplash.com/collection/430471/
overlay: blue
published: true
---

##BFG tool to simplify .git repo
download page
```
https://rtyley.github.io/bfg-repo-cleaner/
```
usage:
```
java -jar bfg-1.14.0.jar -b 2M mmagnn/.git
```
if protected commits append the command
--no-blob-protection
```
java -jar bfg-1.14.0.jar -b 2M mmagnn/.git --no-blob-protection
```