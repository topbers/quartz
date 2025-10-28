---
date: 2025-10-28
---
- 이호진(2020), 『Git 교과서』 , 길벗. 

> [!tip] Git and GitHub
> 딱히 다른 프로그래머와 협업할 일까지는 없을 듯하지만 깃헙에서 쓸만한 코드들은 쏙쏙 배워오기 위해 기본 지식 습득하기. 나만 알아보면 되는 정도로 간단하게 정리한다.

## Basic (Linux) Grammar

| command             | meaning                                | options                                                                      |
| ------------------- | -------------------------------------- | ---------------------------------------------------------------------------- |
| `mkdir`             | make the folder                        | `-p a/b/c` with parents<br>`-v` check                                        |
| `cd`                | go to the folder                       |                                                                              |
| `mv`                | move `mv [option] [from] [to]`         | `-f` force                                                                   |
| `cp`                | copy `cp [option] [what] [to where]`   | `-r` every (**with git**)<br>`-a`<br>`-f` force<br>`-n` no if already exists |
| `rm`                | remove                                 | `-r` delete dir too<br>`-v` show the process                                 |
| `ls`                | list up the entities within the folder |                                                                              |
| `cat`               | show the content/ "concatenate"        |                                                                              |
| `cmp` `diff` `comm` | comparing / difference / commonalities |                                                                              |
| `code`              | open VS Code                           |                                                                              |

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

## Basic

### Configuration

숨은 폴더로 `.git` 생성 → 이 안에 `.git/config` 파일이 있다. `cat .git/config` 로 내용 확인 가능. 수정은 바깥 폴더에서 `git config [type] "aaa"`로 가능. 여기서 `[type]`는 `user.name` `user.email` 등.

### Working Directory and Stage

- Working Directory: 내 작업공간
	- 여기서 `git add` 하면 stage에 등록 (**tracked**)
	- 파일이 수정되면 그 파일은 modified 상태, unstaged
- staged / unstaged 를 구분하면 되는 듯

### Status

- `git status` 상태 확인 ⋯ 또는
- 소스트리에서 staged / unstaged 파일 

### Gitignore

- `.gitignore` 라는 이름을 가진 파일을 최상위 디렉토리에 생성: 내가 쓸 일은 거의 없겠지만 일단 알아 두기
```
# 만능 문자열
*.obj

# 이건 제외하지 말기는 느낌표로
!config.php

# 이 디렉토리 아래의 모든 .txt 파일
doc/**/*.txt
```

### Clone

공개된 저장소의 URL을 알고, 어디 폴더로 클론해 오고 싶을 때

`git clone URL 새폴더이름`
