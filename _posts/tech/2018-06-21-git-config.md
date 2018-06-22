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
# for auto completion
sudo apt-get install bash-completion

wget https://raw.githubusercontent.com/git/git/master/contrib/completion/git-prompt.sh
mv git-completion.bash .git-completion.bash
echo "source ~/.git-completion.bash" >> .bashrc
```

