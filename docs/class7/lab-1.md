# 실습 7-1. 터미널로 Git 다루기

!!! abstract "이번 실습에서 할 것"
    - 브라우저 속 개발 환경 Codespaces를 열고 터미널에서 Git 명령을 입력합니다.
    - 분기 만들기, add, commit, push를 하나씩 해 보고 웹에서 결과를 확인합니다.
    - .gitignore로 비밀 파일을 빼고, 웹에서 바꾼 내용을 pull로 내려받습니다.

**소요 시간** 약 10분  **실습 장소** 개인 연습 리포지토리 `lunch-practice`  **관련 교안** [웹 동작과 Git 명령](index.md#web-and-git), [네 단계](index.md#four-stages), [.gitignore](index.md#gitignore)

## 준비

- 내 연습 리포지토리 `https://github.com/<내아이디>/lunch-practice`를 엽니다. 팀 리포지토리가 아닙니다.
- 명령어는 아래 코드 블록 오른쪽 위 복사 버튼으로 복사해 터미널에 붙여 넣고 ++enter++를 누르면 됩니다. 터미널에서 붙여 넣기는 ++ctrl+v++(Mac은 ++cmd+v++)이고, 처음에 브라우저가 클립보드 허용을 물으면 **Allow**(허용)를 누릅니다.

## STEP 1. Codespace 열기

Codespaces는 GitHub가 빌려주는 컴퓨터에 VS Code(코드 편집기)를 띄워 브라우저로 보여 주는 기능입니다. 설치할 것이 없습니다.

1. `lunch-practice` 리포지토리 **Code** 탭에서 초록색 **Code** ▼ 버튼 클릭
2. 위쪽 **Codespaces** 탭 클릭
3. **Create codespace on main**(main 분기로 Codespace 만들기) 클릭
4. 새 탭이 열리고 "Setting up your codespace" 화면이 나옵니다. 1~2분 기다립니다.

화면이 열리면 이렇게 생겼습니다.

| 위치 | 무엇이 있나 |
|---|---|
| 왼쪽 | 파일 목록(Explorer). `README.md`, `docs`, `site` 등 리포지토리 파일이 보입니다 |
| 가운데 | 파일을 클릭하면 열리는 편집기 |
| 아래 | **터미널**. `@아이디 ➜ /workspaces/lunch-practice (main) $` 같은 줄이 보이고, 여기에 명령을 입력합니다 |

터미널이 안 보이면 키보드 ++ctrl+grave++(Esc 아래 물결표 키)를 누르거나, 왼쪽 위 메뉴(☰) → **Terminal** → **New Terminal**을 클릭합니다.

확인: 아래쪽 터미널에 `(main) $`로 끝나는 줄이 보입니다. 괄호 안이 지금 분기 이름입니다.

!!! note "사용자 이름과 메일을 설정하라고 하지 않나요?"
    내 컴퓨터에서 Git을 처음 쓰면 `git config --global user.name`으로 이름과 메일을 설정해야 합니다. Codespaces는 GitHub 계정 정보로 **자동 설정**되어 있어서 이 단계가 없습니다. 로그인 인증도 자동입니다.

## STEP 2. 지금 상태와 이력 보기

1. 지금 상태를 봅니다.

    ```bash
    git status
    ```

    ```text
    On branch main
    Your branch is up to date with 'origin/main'.

    nothing to commit, working tree clean
    ```

    "main 분기에 있고, GitHub(origin)와 같고, 바뀐 것이 없다"는 뜻입니다.

2. 최근 커밋 5개를 한 줄씩 봅니다.

    ```bash
    git log --oneline -5
    ```

    ```text
    e4f5a6b (HEAD -> main, origin/main) Revert "메뉴 가격 변경"
    9c8d7e6 Merge pull request #3 from 내아이디/add-menu
    3b2a1c0 README에 서비스 소개와 그림 추가
    7d6e5f4 김치찌개 가격 9000원으로 수정
    1a2b3c4 Initial commit
    ```

    해시와 메시지는 사람마다 다릅니다. 1~3교시에 웹에서 만든 커밋들이 그대로 보입니다. **History** 화면과 같은 내용입니다. 목록이 화면을 넘어가서 `:`가 보이면 ++q++를 눌러 빠져나옵니다.

확인: 오전에 웹에서 만든 커밋 메시지가 터미널에 보입니다.

## STEP 3. 분기 만들고 파일 고치기

1. 새 분기를 만들고 이동합니다.

    ```bash
    git switch -c terminal-practice
    ```

    ```text
    Switched to a new branch 'terminal-practice'
    ```

    터미널 줄 끝이 `(terminal-practice) $`로 바뀝니다.

2. 왼쪽 파일 목록에서 `docs` → `my-note.md`를 클릭해 엽니다. 파일이 없으면 `docs` 폴더에 마우스 오른쪽 클릭 → **New File...** → `my-note.md` 입력 후 ++enter++
3. 맨 아래에 한 줄을 추가합니다.

    ```markdown
    - 터미널에서 처음으로 커밋해 봤습니다.
    ```

4. 저장합니다. Windows는 ++ctrl+s++, Mac은 ++cmd+s++. 탭 이름 옆 흰 점이 사라지면 저장된 것입니다.
5. 상태를 봅니다.

    ```bash
    git status
    ```

    ```text
    On branch terminal-practice
    Changes not staged for commit:
      (use "git add <file>..." to update what will be committed)
            modified:   docs/my-note.md
    ```

    `modified`(고쳐짐)가 **빨간색**입니다. 작업 폴더에서 고쳤지만 아직 장바구니(스테이징)에 담지 않은 상태입니다. 새로 만든 파일이라면 `Untracked files:`(Git이 아직 모르는 파일) 아래 빨간색으로 나옵니다.

확인: `docs/my-note.md`가 빨간색으로 보입니다.

## STEP 4. 담고(add), 기록하고(commit), 올리기(push)

1. 파일을 스테이징에 담습니다.

    ```bash
    git add docs/my-note.md
    git status
    ```

    ```text
    On branch terminal-practice
    Changes to be committed:
      (use "git restore --staged <file>..." to unstage)
            modified:   docs/my-note.md
    ```

    이번에는 **초록색**입니다. "커밋될 변경(Changes to be committed)"에 담겼습니다.

2. 커밋합니다. `-m` 뒤가 커밋 메시지입니다.

    ```bash
    git commit -m "터미널에서 메모 추가"
    ```

    ```text
    [terminal-practice 5f6e7d8] 터미널에서 메모 추가
     1 file changed, 1 insertion(+)
    ```

3. 이력을 다시 봅니다.

    ```bash
    git log --oneline -3
    ```

    ```text
    5f6e7d8 (HEAD -> terminal-practice) 터미널에서 메모 추가
    e4f5a6b (origin/main, main) Revert "메뉴 가격 변경"
    9c8d7e6 Merge pull request #3 from 내아이디/add-menu
    ```

    새 커밋 옆에 `origin`이 없습니다. 아직 내 컴퓨터(로컬)에만 있고 GitHub에는 없다는 뜻입니다.

4. GitHub에 올립니다. `-u`는 "이 분기를 GitHub의 같은 이름 분기와 연결해 두라"는 뜻이라 처음 한 번만 붙입니다.

    ```bash
    git push -u origin terminal-practice
    ```

    ```text
    ...
     * [new branch]      terminal-practice -> terminal-practice
    branch 'terminal-practice' set up to track 'origin/terminal-practice'.
    ```

5. 브라우저의 `lunch-practice` 탭으로 돌아가 새로 고침 → 분기 버튼(`main` ▼) 클릭 → `terminal-practice`가 있는지 확인 → 선택 → `docs/my-note.md`를 열어 추가한 줄을 확인합니다. 위쪽에 노란 띠 **Compare & pull request**가 보여도 이번에는 PR을 만들지 않습니다.

확인: 웹에서 `terminal-practice` 분기와 "터미널에서 메모 추가" 커밋이 보입니다.

!!! note "왜 이렇게 하나요?"
    웹에서는 **Commit changes** 한 번이었던 일이 add, commit, push 세 번으로 나뉩니다. [교안의 네 단계 그림](index.md#four-stages)에서 화살표 하나씩을 직접 건넌 것입니다.

## STEP 5. .gitignore로 비밀 파일 빼기

실습 전에 설명한 [.gitignore 교안](index.md#gitignore)을 직접 확인하는 단계입니다. Git이 무시할 파일 이름을 적어 두면, 그 파일은 `git add`를 해도 담기지 않습니다.

1. 비밀번호가 든 파일을 흉내 내어 만듭니다. (진짜 비밀번호를 쓰지 마세요.)

    ```bash
    echo "PASSWORD=1234" > .env
    git status
    ```

    ```text
    On branch terminal-practice
    Untracked files:
            .env
    ```

    `.env`가 빨간색으로 보입니다. 이 상태에서 `git add .`(모든 파일 담기)를 하면 비밀번호 파일이 커밋되어 GitHub에 올라갑니다.

2. 무시할 파일 목록 `.gitignore`를 만듭니다.

    ```bash
    echo ".env" > .gitignore
    git status
    ```

    ```text
    On branch terminal-practice
    Untracked files:
            .gitignore
    ```

    `.env`가 목록에서 **사라지고** `.gitignore`만 보입니다. Git이 `.env`를 무시하기 시작했습니다. 왼쪽 파일 목록에서도 `.env`는 흐린 회색으로 보입니다.

3. `.gitignore`를 담고, 기록하고, 올립니다. 이번에는 `-u`가 필요 없습니다.

    ```bash
    git add .gitignore
    git commit -m ".env 파일을 Git에서 제외"
    git push
    ```

4. 웹에서 `terminal-practice` 분기를 새로 고침해 `.gitignore`는 있고 `.env`는 **없는** 것을 확인합니다.

확인: 웹의 `terminal-practice` 분기에 `.gitignore`만 있고 `.env`는 없습니다.

## STEP 6. 웹에서 바꾸고 pull로 내려받기

다른 팀원이 GitHub에 커밋을 올린 상황을 흉내 냅니다.

1. 브라우저의 `lunch-practice` 탭에서 분기가 `terminal-practice`인지 확인하고 `README.md` 클릭 → 연필 아이콘
2. 맨 아래에 한 줄 추가합니다.

    ```markdown
    웹에서 추가한 줄입니다. 터미널에서 pull로 받아 보세요.
    ```

3. **Commit changes...** → 메시지 `웹에서 README 한 줄 추가` → **Commit directly to the terminal-practice branch** 확인 → **Commit changes**
4. Codespace 탭으로 돌아와 터미널에서 내려받습니다.

    ```bash
    git pull
    ```

    ```text
    Updating 8a9b0c1..2d3e4f5
    Fast-forward
     README.md | 2 ++
     1 file changed, 2 insertions(+)
    ```

5. 파일 내용을 터미널에서 확인합니다.

    ```bash
    cat README.md
    ```

    맨 아래에 "웹에서 추가한 줄입니다."가 보이면 성공입니다.

확인: 웹에서 추가한 줄이 Codespace의 `README.md`에 보입니다.

## STEP 7. Codespace 정리하기

Codespace는 켜 둔 시간만큼 무료 사용량을 씁니다. 실습이 끝나면 중지하고 삭제합니다. 커밋은 이미 GitHub에 push했으니 지워도 안전합니다.

1. 브라우저에서 `https://github.com/codespaces` 접속
2. 목록에서 `lunch-practice` Codespace 오른쪽 **...** 클릭 → **Stop codespace**(중지) 클릭
3. 다시 **...** → **Delete**(삭제) 클릭 → 확인 창에서 **Delete** 클릭
4. Codespace 브라우저 탭을 닫습니다.

!!! info "무료 사용 시간"
    개인 무료 계정은 매달 Codespaces 사용량이 정해져 있습니다(2코어 기준 약 60시간, 저장 공간 15GB). 30분 동안 아무것도 안 하면 자동으로 중지되지만, 삭제하지 않으면 저장 공간을 계속 씁니다. 회사 계정은 회사 정책을 따릅니다.

확인: `https://github.com/codespaces`에 `lunch-practice` Codespace가 없습니다.

## 성공하면

- [x] Codespace를 열고 터미널에서 `git status`, `git log --oneline -5`를 실행했다
- [x] `terminal-practice` 분기를 만들고 add 전후로 빨간색과 초록색 상태를 보았다
- [x] commit, push 후 웹에서 분기와 커밋을 확인했다
- [x] `.gitignore`로 `.env`를 뺐고, 웹에 `.env`가 올라가지 않았다
- [x] 웹에서 바꾼 README를 `git pull`로 내려받았다
- [x] Codespace를 중지하고 삭제했다

## 막히면

??? failure "터미널이 안 보여요"
    ++ctrl+grave++를 누르거나 왼쪽 위 메뉴(☰) → **Terminal** → **New Terminal**을 클릭합니다. 아래쪽 패널이 접혀 있으면 화면 아래 경계선을 위로 끌어올립니다.

??? failure "Codespace가 몇 분째 Setting up에서 멈춰 있어요"
    탭을 새로 고침합니다. 그래도 안 되면 `https://github.com/codespaces`에서 그 Codespace를 삭제하고 다시 만듭니다. 회사망에서 막힌 경우라면 강사에게 알려 주세요.

??? failure "git push가 거부돼요 (rejected, permission denied)"
    `rejected ... (fetch first)`는 GitHub에 내 컴퓨터에 없는 커밋이 있다는 뜻입니다. `git pull`을 먼저 하고 다시 `git push`합니다. `Permission denied`나 `403`은 다른 사람 리포지토리에서 Codespace를 연 경우입니다. 내 `lunch-practice`에서 열었는지 확인하세요.

??? failure "git commit에서 'Please tell me who you are'가 나와요"
    Codespaces에서는 보통 나오지 않습니다. 나오면 아래 두 줄을 실행한 뒤 다시 커밋합니다.

    ```bash
    git config --global user.name "내 이름"
    git config --global user.email "내아이디@users.noreply.github.com"
    ```

??? failure "git status에 docs/my-note.md가 안 나와요"
    파일을 저장하지 않은 경우입니다. 편집기 탭 이름 옆에 흰 점이 있으면 ++ctrl+s++(Mac은 ++cmd+s++)로 저장하세요.

??? failure "git log 화면에서 빠져나올 수가 없어요"
    아래에 `:`나 `(END)`가 보이면 ++q++를 누릅니다.

??? failure "git pull에서 편집기 화면이 열리거나 'divergent branches' 메시지가 나와요"
    웹에서 커밋하기 전에 터미널에서도 커밋을 하나 더 만든 경우입니다. 편집기가 열렸다면 그대로 닫고, 메시지가 나왔다면 `git pull --no-rebase`를 실행합니다. 모르겠으면 강사에게 화면을 보여 주세요.

## 다음 실습으로 넘어가기 전에

- `lunch-practice`의 `terminal-practice` 분기는 지우지 않아도 됩니다. 복습할 때 다시 Codespace를 열어 써 보세요.
- 다음 [실습 7-2](lab-2.md)는 **팀 리포지토리**에서 합니다.
