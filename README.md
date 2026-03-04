# ASE 2026 论文项目

面向 RISC-V 构建失败根因分析的日志压缩与规则学习方法（ACM sigconf 模板）。

## 项目结构

- `ase2026.tex` — 主论文 LaTeX 源文件
- `reference.bib` — 参考文献
- `pic/` — 论文图片
- `参考/` — 参考资料与论文图源文件

## 编译

使用 XeLaTeX 编译（需中文字体，如 SimSun）：

```bash
xelatex ase2026
bibtex ase2026
xelatex ase2026
xelatex ase2026
```

或使用 latexmk：

```bash
latexmk -xelatex ase2026.tex
```

## 协作

克隆后在本仓库中直接编辑并提交，通过 Pull Request 或共同维护分支进行协作。
