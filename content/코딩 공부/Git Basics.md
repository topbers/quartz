## Hidden Folder .git

숨은 폴더로 `.git` 생성 → 이 안에 `.git/config` 파일이 있다. `cat .git/config` 로 내용 확인 가능. 수정은 바깥 폴더에서 `git config [type] "aaa"`로 가능. 여기서 `[type]`는 `user.name` `user.email` 등.

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

## Working Directory and Stage

- Working Directory: 내 작업공간
	- 여기서 `git add` 하면 stage에 등록 (**tracked**)
	- 파일이 수정되면 그 파일은 modified 상태, unstaged
- staged / unstaged 를 구분하면 되는 듯

## Git Commands

| command                                                               | meanings                                          |
| --------------------------------------------------------------------- | ------------------------------------------------- |
| `git status`                                                          | 상태 확인                                             |
| `git log`                                                             | 로그                                                |
| `git add [filename]`                                                  | ① 이 파일을 스테이지 영역으로 등록                              |
| `git rm --cached [filename]`                                          | ~① 스테이지 영역의 파일을 등록 취소                             |
| `git mv [oldfilename] [newfilename]`                                  | ①' 파일 이름 변경                                       |
| `git commit -m "message"`<br>`git commit --allow-empty-message -m ""` | ② 스테이지 영역의 파일을 커밋 ("커밋 메시지")<br>메시지 없이 커밋하고 싶을 경우 |
| `git commit -a`                                                       | ①+② 등록과 커밋을 동시에                                   |
| `git checkout -- [filename]`                                          | ②' 수정한 파일을 마지막 커밋으로 복귀                            |
| `git diff`<br>`git diff head`                                         | 스테이지-언스테이지 비교<br>스테이지-헤드 비교                       |

## Clone

공개된 저장소의 URL을 알고, 어디 폴더로 클론해 오고 싶을 때 `git clone URL 새폴더이름`