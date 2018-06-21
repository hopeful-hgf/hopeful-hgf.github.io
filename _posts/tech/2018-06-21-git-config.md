---
layout: post
title: git 安装之后的配置
category: 技术
tags: linux git
keywords: debian;git;config
description: 
---

```bash
git config --global user.email "xxx@"
git config --global user.name "xx"
git config --global alias.pgh "push origin"
wget https://github.com/git/git/blob/master/contrib/completion/git-completion.bash
mv git-completion.bash .git-completion.bash
echo "source ~/.git-completion.bash" >> .bashrc
```

