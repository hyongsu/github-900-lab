# 실습 1-2. 템플릿으로 연습 리포지토리 만들기

!!! abstract "이번 실습에서 할 것"
    - Starter 템플릿으로 오늘 하루 계속 쓸 연습 리포지토리 `lunch-practice`를 만듭니다.
    - 실습 1-1의 빈 리포지토리와 무엇이 다른지 파일 목록과 커밋 수로 비교합니다.
    - GitHub Pages를 켜고 배포를 실행해 "점심 메뉴 추천" 웹페이지를 엽니다.

**소요 시간** 약 7분  **실습 장소** 개인 연습 리포지토리 `lunch-practice`  **관련 교안** [1교시 교안](index.md#account-types)

## 준비

- [실습 1-1](lab-1.md)에서 `my-first-repo`를 만들고 커밋해 봤어야 합니다.
- 이 실습에서 만드는 `lunch-practice`는 1교시부터 4교시, 그리고 7교시까지 계속 씁니다. **오늘 수업이 끝날 때까지 지우지 마세요.**

## STEP 1. Starter 템플릿 열기

실습 1-1에서는 빈 리포지토리에서 시작했습니다. 이번에는 강사가 파일을 미리 넣어 둔 Starter 리포지토리를 본떠서 만듭니다. Starter는 **템플릿**(template)으로 설정되어 있어서, 내용을 그대로 복사한 내 리포지토리를 새로 만들 수 있습니다.

1. 브라우저 주소창에 아래 주소를 입력하고 ++enter++ 를 누릅니다.

    ```text
    https://github.com/skilleat-labs/lunch-picker-starter
    ```

2. 화면 위쪽에 `skilleat-labs / lunch-picker-starter`라는 이름과 **Public template**이라는 표시가 보이는지 확인합니다. `skilleat-labs`는 강사가 실습 자료를 올려 둔 계정입니다.

확인: 파일 목록 위쪽 오른편에 초록색 **Use this template**(이 템플릿 사용) 버튼이 보입니다.

## STEP 2. 템플릿으로 내 리포지토리 만들기

1. 초록색 **Use this template** 버튼을 클릭합니다.
2. 펼쳐진 메뉴에서 **Create a new repository**(새 리포지토리 만들기)를 클릭합니다.
3. 실습 1-1에서 본 것과 같은 "Create a new repository" 화면이 열립니다. 위쪽 **Start with a template** 칸에 `skilleat-labs/lunch-picker-starter`가 이미 골라져 있습니다. 아래 표대로 입력합니다.

    | 항목 | 입력하거나 고를 값 | 설명 |
    |---|---|---|
    | **Include all branches** | 체크하지 않음 (기본값 그대로) | 템플릿의 main 분기만 가져옵니다 |
    | **Owner** | 내 GitHub 아이디 | 조직 이름이 보여도 고르지 않습니다 |
    | **Repository name** | `lunch-practice` | 아래 코드 블록을 복사해서 붙여 넣으세요 |
    | 공개 범위 | **Public** | 오늘 실습은 모두 공개 리포지토리로 합니다 |

    ```text
    lunch-practice
    ```

4. 화면 맨 아래 초록색 **Create repository** 버튼을 클릭합니다.
5. 몇 초 동안 "Generating your repository..." 화면이 보였다가 새 리포지토리로 이동합니다.

확인: 화면 위쪽에 `내아이디 / lunch-practice`가 보이고, 그 아래에 작은 글씨로 `generated from skilleat-labs/lunch-picker-starter`가 보입니다.

!!! success "빨간 X와 All checks have failed가 보여도 정상입니다"
    리포지토리를 만들고 10초쯤 지나면 아래 표시가 생깁니다. **잘못 만든 것이 아닙니다.** 그대로 다음 STEP으로 넘어갑니다.

    | 어디에 | 무엇이 보이나 |
    |---|---|
    | 파일 목록 위 회색 줄 | `Initial commit` 옆에 빨간 **X** |
    | 빨간 X를 누르면 | `All checks have failed`, `웹페이지 배포 / deploy (push) Failing after 6s` |
    | 오른쪽 **Deployments** | `github-pages` 앞에 빨간 표시 |

    **왜 실패하나요?** 리포지토리를 만드는 순간 `Initial commit`이 생기고, 그 커밋을 계기로 Starter에 들어 있는 **웹페이지 배포** 작업이 바로 한 번 돕니다. 그런데 템플릿으로 만든 리포지토리에는 Pages(웹페이지 호스팅) 설정이 따라오지 않습니다. Pages가 꺼진 상태에서 배포를 시도했으니 `Get Pages site failed`(Pages 사이트를 찾을 수 없음) 오류로 실패한 것입니다.

    **언제 없어지나요?** STEP 4에서 Pages를 켜고 STEP 5에서 배포를 다시 실행하면 초록 체크가 됩니다. 처음 실패한 `Initial commit` 기록은 빨간 X로 남아 있어도 괜찮습니다.

!!! note "왜 Public으로 만드나요?"
    오늘 쓰는 무료(Free) 요금제에서는 공개 리포지토리여야 GitHub Pages 웹페이지, 분기 보호 같은 기능을 모두 쓸 수 있습니다. 실습 파일에는 개인 정보가 없으니 공개해도 괜찮습니다. 회사 업무 리포지토리는 회사 규정에 따라 Private(비공개)로 만듭니다.

## STEP 3. 빈 리포지토리와 비교해 보기

방금 만든 `lunch-practice` 첫 화면(**Code** 탭)을 실습 1-1의 `my-first-repo`와 비교합니다.

| 비교 | `my-first-repo` (실습 1-1) | `lunch-practice` (지금) |
|---|---|---|
| 만든 방법 | 빈 리포지토리 + README | Starter 템플릿 복사 |
| 파일 | `README.md` 하나 | `.github`, `docs`, `scripts`, `site`, `README.md` |
| 커밋 수 | 2 Commits (내가 하나 더 커밋) | **1 Commit** |

1. 파일 목록을 봅니다. 각 폴더는 아래와 같습니다.

    | 이름 | 무엇인가 |
    |---|---|
    | `.github` | 자동 작업(Actions) 설정이 들어 있는 폴더 |
    | `docs` | 현업 요청, 킥오프 회의록, 현행 업무 문서 |
    | `scripts` | 메뉴 데이터를 검사하는 프로그램 |
    | `site` | 점심 메뉴 추천 웹페이지 (`index.html`, `menus.json`) |
    | `README.md` | 리포지토리 소개 문서. 2교시에 꾸밉니다 |

2. 파일 목록 위 회색 줄 오른쪽 끝이 **1 Commit**인지 봅니다.

확인: 커밋 수가 **1 Commit**입니다. 템플릿으로 만들면 Starter의 이력은 따라오지 않고, 지금 상태의 파일이 모두 담긴 커밋 1개로 새로 시작합니다.

## STEP 4. GitHub Pages 켜기

`site/` 폴더에 웹페이지 파일이 들어 있습니다. **GitHub Pages**는 리포지토리의 파일로 웹사이트를 무료로 열어 주는 기능입니다. 템플릿으로 만든 리포지토리는 이 설정이 꺼진 채로 시작하므로 직접 켭니다.

1. 리포지토리 위쪽 탭에서 **Settings**(설정)를 클릭합니다. 탭이 안 보이면 탭 줄 오른쪽 끝의 **...** 을 눌러 찾습니다.
2. 왼쪽 메뉴를 아래로 내려 **Code and automation** 묶음 아래의 **Pages**를 클릭합니다.
3. **Build and deployment** 영역의 **Source** 드롭다운을 클릭하고 **GitHub Actions**를 고릅니다. 따로 저장 버튼은 없습니다. 고르는 즉시 저장됩니다.

확인: **Source**가 `GitHub Actions`로 바뀌어 있습니다.

!!! warning "Use a suggested workflow, Configure 버튼은 누르지 않습니다"
    Source를 GitHub Actions로 바꾸면 아래에 Jekyll, Static HTML 같은 추천 작업 카드와 **Configure** 버튼이 나올 수 있습니다. 우리 리포지토리에는 이미 배포 작업(`.github/workflows/pages.yml`)이 있으므로 아무것도 누르지 않습니다.

## STEP 5. 배포 작업 실행하기

Starter에는 `main`에 커밋이 생기면 `site/` 폴더를 웹페이지로 배포하는 자동 작업(**웹페이지 배포**)이 들어 있습니다. Pages를 켰으니 이 작업을 한 번 직접 실행합니다.

1. 리포지토리 위쪽 탭에서 **Actions**를 클릭합니다.
2. 목록에 `Initial commit`이라는 실행 기록이 **빨간 X**로 보일 수 있습니다. STEP 2 뒤에서 본 그 실패입니다. 정상입니다.
3. 왼쪽 **All workflows** 아래 목록에서 **웹페이지 배포**를 클릭합니다.
4. 오른쪽의 **Run workflow** 버튼을 클릭합니다. 펼쳐진 창에서 **Use workflow from**이 `Branch: main`인지 확인하고, 초록색 **Run workflow** 버튼을 클릭합니다.
5. 몇 초 뒤 목록 맨 위에 새 실행 기록이 노란 원(실행 중)으로 나타납니다. 나타나지 않으면 새로고침합니다.
6. 1~2분 기다리면 노란 원이 초록 체크로 바뀝니다.

확인: 새 실행 기록 왼쪽에 **초록 체크**가 보입니다.

!!! note "이번에는 왜 성공하나요?"
    처음 실행은 Pages가 꺼져 있어서 실패했고, STEP 4에서 Pages를 켠 뒤 다시 실행했으니 이번에는 성공합니다. 이렇게 **커밋을 계기로 자동으로 도는 작업**을 GitHub Actions라고 하고, 3교시와 6교시에 다시 봅니다.

## STEP 6. 웹페이지 열기

1. **Settings** → **Pages**로 다시 갑니다.
2. 화면 위쪽에 `Your site is live at`라는 문구와 함께 주소가 보입니다.

    ```text
    https://<내아이디>.github.io/lunch-practice/
    ```

3. 주소 옆의 **Visit site** 버튼을 클릭합니다. (새 탭에서 열립니다.)
4. "점심 메뉴 추천" 웹페이지에서 아래 내용을 확인합니다.
    - 파란 머리말에 `점심 메뉴 추천`, `오늘 점심, 5분 안에 정해 봅시다.`
    - 메뉴 카드 **6개**: 김치찌개, 짜장면, 돈카츠, 샐러드볼, 쌀국수, 순두부찌개
    - 김치찌개 카드의 가격 **9,000원**
5. 예산 칸에 `9000`을 입력해 9,000원 이하 메뉴(김치찌개, 짜장면, 순두부찌개)만 남는지, **아무거나 골라 줘** 버튼을 누르면 "오늘의 추천: ..." 문구가 나오는지 확인합니다.

확인: 메뉴 카드 6개가 보이는 웹페이지가 열립니다. 이 탭은 닫지 말고 열어 두세요. 실습 1-3에서 김치찌개 가격을 고친 뒤 다시 봅니다.

!!! note "웹페이지 내용은 어디서 오나요?"
    `site/index.html`이 화면 모양을, `site/menus.json`이 메뉴 데이터를 담당합니다. 다음 실습에서 `menus.json`의 가격을 고치고 커밋하면, 배포 작업이 자동으로 다시 돌아서 웹페이지에도 반영됩니다.

## 성공하면

- [x] `https://github.com/<내아이디>/lunch-practice` 리포지토리가 있습니다. Public이고, **1 Commit**입니다.
- [x] **Settings** → **Pages**의 Source가 `GitHub Actions`입니다.
- [x] **Actions** 탭의 **웹페이지 배포** 최신 실행이 초록 체크입니다.
- [x] `https://<내아이디>.github.io/lunch-practice/`에서 메뉴 카드 6개가 보입니다.

## 막히면

??? failure "Use this template 버튼이 안 보입니다"
    로그인이 안 되어 있거나, 주소를 잘못 입력해서 다른 리포지토리에 들어온 경우입니다. 오른쪽 위에 프로필 사진이 있는지 확인하고, 주소가 정확히 `https://github.com/skilleat-labs/lunch-picker-starter`인지 확인합니다. 브라우저 창이 좁으면 버튼이 아래로 밀려 있을 수 있으니 창을 넓혀 봅니다.

??? failure "The repository lunch-practice already exists on this account 라고 나옵니다"
    같은 이름의 리포지토리가 이미 있습니다. 예전에 연습으로 만들었다면 그 리포지토리를 쓰지 말고 강사에게 알려 주세요. 강사 안내에 따라 기존 것을 Settings 맨 아래 **Delete this repository**로 지운 뒤 다시 만들거나, 이름 뒤에 숫자를 붙입니다. 이름을 바꾼 경우 이후 실습의 `lunch-practice`를 내 리포지토리 이름으로 바꿔 읽으면 됩니다.

??? failure "Owner 드롭다운에 회사 조직 이름이 기본으로 선택되어 있습니다"
    드롭다운을 눌러 **내 아이디**로 바꿉니다. 조직 아래에 만들면 웹페이지 주소와 권한이 달라져서 이후 실습이 꼬입니다.

??? failure "Settings 탭이 없습니다"
    내 리포지토리가 아니라 Starter(`skilleat-labs/lunch-picker-starter`) 화면에 있는 경우입니다. 주소창이 `github.com/<내아이디>/lunch-practice`인지 확인합니다.

??? failure "Run workflow 버튼이 안 보입니다"
    왼쪽 목록에서 **웹페이지 배포**를 클릭하지 않고 **All workflows**에 머물러 있는 경우입니다. 왼쪽에서 **웹페이지 배포**를 먼저 클릭합니다. Actions 탭에 "Workflows aren't being run on this repository" 같은 안내와 초록 버튼이 보이면 **I understand my workflows, go ahead and enable them**을 눌러 켠 뒤 다시 시도합니다.

??? failure "Pages를 켰는데 Actions에 아직 Get Pages site failed 오류가 보입니다"
    지금 보고 있는 것이 **리포지토리를 만들 때 돈 예전 실행 기록**(`Initial commit`)인지 확인합니다. Pages를 켠다고 예전 기록이 다시 실행되지는 않습니다. 그 기록은 빨간 X로 남겨 두고, STEP 5대로 **웹페이지 배포** → **Run workflow**를 눌러 **새 실행**을 만듭니다. 목록 맨 위에 새 기록이 생겨 초록 체크가 되면 성공입니다.

    같은 화면의 `Node.js 20 is deprecated`, `The ubuntu-latest label will migrate` 같은 노란 경고는 GitHub가 보내는 안내 문구입니다. 실패 원인이 아니니 무시합니다.

??? failure "Run workflow를 눌렀는데 또 빨간 X입니다"
    **Settings** → **Pages**의 Source가 `GitHub Actions`로 바뀌었는지 다시 확인합니다. 바뀌어 있다면 빨간 X 실행 기록을 클릭하고, 오른쪽 위 **Re-run jobs** → **Re-run all jobs**를 눌러 한 번 더 실행합니다.

??? failure "Pages 화면에 주소가 안 보이거나, 주소를 열면 404가 나옵니다"
    배포가 끝난 지 얼마 안 되면 1~2분 정도 404가 보일 수 있습니다. 잠시 기다린 뒤 새로고침합니다. 그래도 안 되면 **Actions** 탭에서 **웹페이지 배포** 최신 실행이 초록 체크인지 확인합니다. 초록 체크인 실행을 클릭하면 `deploy` 상자 아래에도 웹페이지 주소가 보입니다.

## 다음 실습으로 넘어가기 전에

- `lunch-practice` 리포지토리 탭과 웹페이지 탭을 둘 다 열어 둡니다.
- 리포지토리는 오늘 끝까지 씁니다. 지우거나 이름을 바꾸지 않습니다.
