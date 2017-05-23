
# Setup ThuThesis (on Win8.1)

[toc]

ThuThesis is a LaTeX template for undergrad/grad/postdoc thesis work at Tsinghua University.

## Installation

See [github repo of THUThesis](https://github.com/xueruini/thuthesis)

## Problems I met and solutions

I was trying to use [ThuThesis](https://github.com/xueruini/thuthesis) on Windows8.1 machine with `CTeX_2.9.2.164` installed.

When trying command `xelatex main`(in Windows command line within the THUThesis folder), I got a bunch of `Undefined control sequence` error about `\ctexset` command and about Chinese characters inside the `thuthesis.cfg` file. So I tried manually including ctex package, but it not only didn't solve the problem but cause more error about multidefinition of some command. After google and stackexchange, I thought I should update MiKTeX.

When running the update for the first time, I noticed only some default selected packages are to be update, and I couldn't check the `select all` box. After the update, xelatex broke down with some error about lack of dll files, in my case `icule44.dll` and `icuuc44.dll` (and more because I stopped downloading them). I felt bad downloading dll files one by one so I went to check the update again and now the `select all` box worked. After waiting until all packages are up to date, xelatex is alive.

However the `xelatex main` still fails. I went through the error message and found that it's due to lack of packages and failure of auto-installation. Installing `dvipdfmx` and `miktex-dvipdfmx-bin-2.9` via the package manager, ThuThesis finally worked.

## Tips

- Error messages are very important!
- Check the MiKTeX update twice or more
- Packages displayed in the package manager are not only the installed ones but are all available packages.




> Written with [StackEdit](https://stackedit.io/).