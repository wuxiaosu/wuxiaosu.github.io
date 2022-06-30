---
title: "git 常用操作"
date: 2021-04-18T10:18:00+08:00
draft: false
tags: ["git"]
---
# git

- Git 回退到某个 commit  

```bash
git reset --hard HEAD^ 回退到上个版本
git reset --hard HEAD~3 回退到前3次提交之前，以此类推，回退到n次提交之前  
git reset --hard commit_id  退到/进到 指定commit的sha码  
```

- 强推到远程:

```bash
git push origin HEAD --force  
```

- 合并某个提交:

```bash
git cherry-pick <commit id> 
```

- 查看本地分支：

```bash
git branch
```

- 删除本地分支：

```bash
git branch -D tmp
```

- 查看 tag：

```bash
git tag
```

- 在某个 commit 上打 tag：

```bash
git tag test_tag c809ddbf83939a89659e51dc2a5fe183af384233
```

- 本地 tag 推送到线上：

```bash
git push origin test_tag
```

- 本地删除 tag：

```bash
git tag -d test_tag
```

- 删除线上 tag：

```bash
git push origin :refs/tags/test_tag
```

- 修改远程地址先删后加

```bash
git remote rm origin
git remote add origin [url]
```

- 创建新分支

```bash
git branch develop
```

- 切换到该分支

```bash
git checkout develop
```

- 提交到该分支

```bash
git push -u origin develop
```

- 修改源

```bash
git remote set-url origin url
```