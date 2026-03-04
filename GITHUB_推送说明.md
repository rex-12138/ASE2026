# 将本仓库推送到 GitHub 的步骤

本地 Git 已初始化并完成首次提交，按下面步骤即可把项目推到 GitHub 并与他人协作。

## 1. 在 GitHub 上创建新仓库

1. 打开 [https://github.com/new](https://github.com/new)
2. **Repository name**：填仓库名，例如 `ASE2026` 或 `ase2026-paper`
3. **Description**（可选）：例如「ASE 2026 论文：面向 RISC-V 构建失败根因分析的日志压缩与规则学习」
4. 选择 **Public**
5. **不要**勾选 “Add a README file”、“Add .gitignore” 或 “Choose a license”（本地已有内容）
6. 点击 **Create repository**

## 2. 在本地添加远程并推送

创建好空仓库后，GitHub 会显示仓库地址，形如：

- HTTPS: `https://github.com/你的用户名/仓库名.git`
- SSH: `git@github.com:你的用户名/仓库名.git`

在项目目录下打开 **命令提示符（cmd）** 或 **PowerShell**，执行（把下面的地址换成你的实际地址）：

```bash
cd c:\Users\DELL\Desktop\ASE2026

# 添加远程仓库（二选一）
git remote add origin https://github.com/你的用户名/仓库名.git
# 若使用 SSH：
# git remote add origin git@github.com:你的用户名/仓库名.git

# 推送（主分支名可能是 master 或 main，按你本地为准）
git branch -M main
git push -u origin main
```

若你本地默认分支是 `master` 且不想改名，可改为：

```bash
git push -u origin master
```

## 3. 邀请协作者

1. 在 GitHub 仓库页面点击 **Settings** → **Collaborators**
2. 点击 **Add people**，输入对方 GitHub 用户名或邮箱
3. 对方接受邀请后即可共同编辑、提交和推送

## 4. 日后提交与推送

修改文件后：

```bash
cd c:\Users\DELL\Desktop\ASE2026
git add -A
git -c commit.gpgsign=false commit -m "简要说明本次修改"
git push
```

若在 PowerShell 下 `git commit` 报错 `unknown option trailer`，可改用 **命令提示符（cmd）** 执行上述命令，或先执行：

```bash
git -c commit.gpgsign=false commit -m "简要说明"
```

再 `git push`。
