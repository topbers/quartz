---
date: 2025-10-28
---
- 이호진(2020), 『Git 교과서』 , 길벗. 

> [!tip] Git and GitHub
> 딱히 다른 프로그래머와 협업할 일까지는 없을 듯하지만 깃헙에서 쓸만한 코드들은 쏙쏙 배워오기 위해 기본 지식 습득하기. 나만 알아보면 되는 정도로 간단하게 정리한다.

우선 [[Linux Grammar]]를 알아야 터미널을 왔다갔다할 수 있다. 마우스 없는 컴퓨터의 디렉토리들을 움직이는 법을 배운다는 느낌으로. [[Git Basics]]에서 지금까지 배운 내용을 내가 알아보기 쉽게 정리했다. 

## Start

터미널에 `git`이라고만 치면 이런 게 나온다. 하나씩 다 알게 되면 마스터?

```
usage: git [-v | --version] [-h | --help] [-C <path>] 
[-c <name>=<value>] [--exec-path[=<path>]] [--html-path] [--man-path] [--info-path] [-p | --paginate | -P | --no-pager] [--no-replace-objects] [--no-lazy-fetch] [--no-optional-locks] [--no-advice] [--bare] [--git-dir=<path>] [--work-tree=<path>] [--namespace=<name>] [--config-env=<name>=<envvar>] <command> [<args>]

These are common Git commands used in various situations:

start a working area (see also: git help tutorial)
   clone      Clone a repository into a new directory
   init       Create an empty Git repository or reinitialize an existing one

work on the current change (see also: git help everyday)
   add        Add file contents to the index
   mv         Move or rename a file, a directory, or a symlink
   restore    Restore working tree files
   rm         Remove files from the working tree and from the index

examine the history and state (see also: git help revisions)
   bisect     Use binary search to find the commit that introduced a bug
   diff       Show changes between commits, commit and working tree, etc
   grep       Print lines matching a pattern
   log        Show commit logs
   show       Show various types of objects
   status     Show the working tree status

grow, mark and tweak your common history
   backfill   Download missing objects in a partial clone
   branch     List, create, or delete branches
   commit     Record changes to the repository
   merge      Join two or more development histories together
   rebase     Reapply commits on top of another base tip
   reset      Reset current HEAD to the specified state
   switch     Switch branches
   tag        Create, list, delete or verify a tag object signed with GPG

collaborate (see also: git help workflows)
   fetch      Download objects and refs from another repository
   pull       Fetch from and integrate with another repository or a local branch
   push       Update remote refs along with associated objects
```

