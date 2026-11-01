# 실습 1-1. 내 첫 리포지토리 만들기

!!! abstract "이번 실습에서 할 것"
    - 내 프로필(`github.com/내아이디`)에서 시작해 빈 리포지토리 `my-first-repo`를 직접 만듭니다.
    - README를 웹에서 고치고 **Commit changes**를 눌러 첫 커밋을 남깁니다.
    - 커밋 수가 1에서 2로 늘고, 이력에 내 커밋이 쌓이는 것을 확인합니다.

**소요 시간** 약 6분  **실습 장소** 내 첫 리포지토리 `my-first-repo`  **관련 교안** [1교시 교안](index.md#my-space)

## 준비

- github.com에 로그인되어 있어야 합니다. 오른쪽 위에 내 프로필 사진이 보이면 로그인된 상태입니다.
- 브라우저 탭 하나만 있으면 됩니다. 설치할 프로그램은 없습니다.
- 이 실습은 "리포지토리를 만들고, 고치고, 커밋하면 기록이 남는다"를 처음 해 보는 연습입니다. 오늘 하루 계속 쓰는 연습 리포지토리 `lunch-practice`는 다음 실습 1-2에서 따로 만듭니다.

## STEP 1. 내 프로필 열기

교안에서 본 것처럼 `github.com/내아이디`가 내 공간입니다. 먼저 그 공간으로 갑니다.

1. 화면 오른쪽 위의 **내 프로필 사진**을 클릭합니다.
2. 펼쳐진 메뉴에서 **Profile**(또는 **Your profile**)을 클릭합니다.
3. 브라우저 주소창을 봅니다. `https://github.com/<내아이디>` 모양입니다.
4. 프로필 이름 아래 탭 줄에서 **Repositories**를 클릭합니다.

확인: 주소창이 `github.com/<내아이디>?tab=repositories`이고, 처음 가입한 계정이라면 리포지토리 목록이 비어 있습니다. 이 실습을 마치면 여기에 `my-first-repo`가 생깁니다.

## STEP 2. 빈 리포지토리 만들기

1. Repositories 목록 오른쪽 위의 초록색 **New** 버튼을 클릭합니다. (화면 오른쪽 위 **+** → **New repository**를 눌러도 같은 화면이 열립니다.)
2. "Create a new repository" 화면이 열립니다. 아래 표대로 입력합니다.

    | 항목 | 입력하거나 고를 값 | 설명 |
    |---|---|---|
    | **Owner** | 내 GitHub 아이디 | 조직 이름이 보여도 고르지 않습니다 |
    | **Repository name** | `my-first-repo` | 아래 코드 블록을 복사해서 붙여 넣으세요 |
    | **Description** | 비워 둠 | 선택 항목입니다 |
    | 공개 범위 (**Choose visibility**) | **Public** | 오늘 실습은 모두 공개 리포지토리로 합니다 |
    | **Add README** | **On**으로 켬 | 화면에 따라 **Add a README file** 체크박스로 보입니다. 체크합니다 |

    ```text
    my-first-repo
    ```

3. Repository name 칸 아래에 초록색으로 `my-first-repo is available.`이 보이는지 확인합니다.
4. 화면 맨 아래 초록색 **Create repository**(리포지토리 만들기) 버튼을 클릭합니다.

확인: 화면 위쪽에 `내아이디 / my-first-repo`가 보이고, 주소창이 `https://github.com/<내아이디>/my-first-repo`입니다. 내 공간(`/내아이디`) 뒤에 리포지토리 이름(`/my-first-repo`)이 붙은 주소입니다.

!!! note "Add README를 왜 켜나요?"
    README를 켜지 않으면 파일이 하나도 없는 정말 빈 리포지토리가 생기고, 첫 화면에 명령어 안내만 잔뜩 보입니다. README를 켜면 GitHub가 `README.md` 파일 하나를 넣고 **첫 커밋**을 대신 만들어 줍니다. 그래서 바로 파일을 열어 고칠 수 있습니다.

## STEP 3. 첫 화면에서 커밋 1개 확인하기

1. 파일 목록에 `README.md` 하나만 있는지 봅니다.
2. 파일 목록 바로 위 회색 줄을 봅니다. 왼쪽에는 내 아이디와 `Initial commit`이라는 메시지가, 오른쪽 끝에는 시계 아이콘과 함께 **1 Commit**이 보입니다. 지금은 **눈으로만** 봅니다. `Initial commit`이나 7자리 번호를 클릭하면 그 커밋 시점의 보기 전용 화면으로 들어가서, 다음 STEP에서 연필 아이콘이 보이지 않습니다.
3. 파일 목록 아래에 README 내용이 펼쳐져 있습니다. 지금은 `my-first-repo`라는 제목 한 줄뿐입니다.

확인: **1 Commit**입니다. 리포지토리를 만든 순간 README를 넣은 커밋 1개가 생겼습니다. 작성자는 나, 메시지는 GitHub가 넣은 `Initial commit`입니다.

## STEP 4. README 고치고 커밋하기

1. 위쪽 리포지토리 이름 `my-first-repo`를 한 번 클릭해 첫 화면으로 갑니다. 그다음 파일 목록에서 **README.md**를 클릭합니다.
2. 왼쪽 위 분기 선택 상자에 **`main`**이 보이는지 확인합니다. `95531ef`처럼 7자리 번호가 보이면 과거 시점 화면이라 고칠 수 없습니다. 분기 선택 상자를 눌러 **main**을 고릅니다.
3. 파일 내용 위쪽 오른편, **Raw** 버튼 옆의 **연필 아이콘**(마우스를 올리면 `Edit this file`)을 클릭합니다.
4. 편집 칸이 열립니다. 첫 줄 `# my-first-repo` 끝을 클릭하고 ++enter++ 를 두 번 누른 뒤, 아래 문장을 입력합니다.

    ```text
    GitHub 첫 연습입니다. 고치고 커밋하면 기록이 남는지 확인합니다.
    ```

5. 아직 저장된 게 아닙니다. 화면 오른쪽 위의 초록색 **Commit changes...**(변경 저장) 버튼을 클릭합니다.
6. **Commit changes** 대화상자가 열립니다. **Commit message** 칸의 기본값을 지우고 아래처럼 씁니다. 기본값은 `Update README.md`이거나, Copilot이 만들어 준 문장(칸 아래에 `Message and description suggested by Copilot.`)일 수 있습니다. **Extended description** 칸에 영어 문장이 미리 들어 있으면 그것도 지웁니다. 오늘은 메시지를 직접 씁니다.

    ```text
    README에 소개 한 줄 추가
    ```

7. 아래 두 선택지 중 **Commit directly to the `main` branch**가 골라져 있는지 확인하고, 초록색 **Commit changes** 버튼을 클릭합니다.

    | 선택지 | 뜻 | 언제 쓰나 |
    |---|---|---|
    | **Commit directly to the `main` branch** | 원본(`main`)에 바로 커밋합니다. 누르는 즉시 리포지토리에 반영됩니다 | 혼자 쓰는 연습 리포지토리. **1~2교시는 이것만 씁니다** |
    | **Create a new branch for this commit and start a pull request** | 원본은 그대로 두고, 사본(분기)을 새로 만들어 거기에 커밋한 뒤 검토 요청(Pull Request)을 엽니다 | 여럿이 쓰는 리포지토리에서 동료 검토를 받을 때. 3교시에 해 봅니다 |

확인: README.md 화면으로 돌아오고, 내용 위 회색 줄에 내 아이디, `README에 소개 한 줄 추가`, `now`(방금)가 보입니다.

!!! warning "Commit changes를 누르지 않고 창을 닫으면"
    편집 칸에서 고친 내용은 Commit changes를 누르기 전까지 어디에도 저장되지 않습니다. 교안의 "Commit changes가 저장 버튼"이 바로 이 뜻입니다.

## STEP 5. 커밋이 쌓인 것 보기

1. 위쪽 리포지토리 이름 `my-first-repo`를 클릭해 첫 화면으로 돌아갑니다.
2. 회색 줄 오른쪽 끝이 **2 Commits**로 바뀌었는지 봅니다. 클릭합니다.
3. 커밋 목록이 최신순으로 보입니다. 맨 위 `README에 소개 한 줄 추가` 메시지를 클릭합니다.
4. 바뀐 내용이 보입니다. 내가 넣은 문장이 앞에 `+`가 붙은 **초록 줄**로 보입니다.

확인: 커밋 목록에 `README에 소개 한 줄 추가`(위)와 `Initial commit`(아래) 2개가 있고, 내 커밋을 열면 추가한 문장이 초록 줄로 보입니다.

| 순서 | 커밋 메시지 | 누가 만들었나 |
|---|---|---|
| 1 (위, 최신) | README에 소개 한 줄 추가 | 내가 STEP 4에서 |
| 2 (아래, 처음) | Initial commit | 리포지토리를 만들 때 GitHub가 |

!!! tip "핵심"
    파일을 고치고 **Commit changes**를 누를 때마다 커밋이 하나씩 쌓입니다. 누가, 언제, 무엇을, 왜(메시지) 바꿨는지가 함께 남습니다. 이력 화면은 실습 1-3에서 더 자세히 봅니다.

## 성공하면

- [x] `https://github.com/<내아이디>/my-first-repo` 리포지토리가 있습니다. Public입니다.
- [x] README에 내가 넣은 소개 문장이 보입니다.
- [x] 첫 화면 커밋 수가 **2 Commits**입니다.
- [x] 커밋 목록 맨 위가 `README에 소개 한 줄 추가`입니다.

## 막히면

??? failure "New 버튼이 안 보입니다"
    다른 사람의 프로필이나 조직 화면에 있는 경우입니다. 오른쪽 위 프로필 사진 → **Profile**로 내 프로필에 들어갔는지 확인합니다. 또는 화면 오른쪽 위 **+** → **New repository**를 누릅니다.

??? failure "The repository my-first-repo already exists on this account 라고 나옵니다"
    예전에 같은 이름으로 만든 리포지토리가 있습니다. 이름 뒤에 숫자를 붙여 `my-first-repo-2`로 만들고 진행합니다.

??? failure "첫 화면에 파일이 없고 Quick setup 명령어만 보입니다"
    STEP 2에서 **Add README**를 켜지 않은 경우입니다. 화면의 **creating a new file** 또는 **README** 링크를 눌러 `README.md`를 만들고 커밋하면 됩니다. 이 경우 STEP 4까지 마치면 커밋 수가 2가 아니라 1일 수 있습니다. 괜찮습니다.

??? failure "README.md 화면에 연필 아이콘이 없습니다"
    왼쪽 위 분기 선택 상자를 봅니다. `main`이 아니라 `95531ef` 같은 7자리 번호가 보이면, 회색 줄의 `Initial commit`이나 번호를 눌러 **과거 시점의 보기 전용 화면**에 들어온 것입니다. 분기 선택 상자를 눌러 **main**을 고르거나, 위쪽 리포지토리 이름 `my-first-repo`를 클릭한 뒤 README.md를 다시 엽니다. 연필 아이콘은 파일 내용 위쪽 오른편 **Raw** 버튼 옆에 있습니다.

??? failure "Commit changes 버튼이 회색이라 눌리지 않습니다"
    아무것도 고치지 않은 상태입니다. 편집 칸에 문장이 들어갔는지 확인합니다.

## 다음 실습으로 넘어가기 전에

- `my-first-repo`는 1교시 연습용입니다. 이후 교시에서는 쓰지 않지만 지우지 않아도 됩니다.
- 다음 실습 1-2에서 오늘 하루 계속 쓸 연습 리포지토리 `lunch-practice`를 만듭니다.
