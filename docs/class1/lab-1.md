# 실습 1-1. 내 연습 리포지토리 만들기

!!! abstract "이번 실습에서 할 것"
    - Starter 템플릿으로 내 연습 리포지토리 `lunch-practice`를 만듭니다.
    - 만들어진 리포지토리 화면에서 파일 목록, README, 커밋 수, 주소를 확인합니다.
    - GitHub Pages를 켜고 첫 배포를 실행해 "점심 메뉴 추천" 웹페이지를 엽니다.

**소요 시간** 약 8분  **실습 장소** 개인 연습 리포지토리 `lunch-practice`  **관련 교안** [1교시 교안](index.md#four-terms)

## 준비

- github.com에 로그인되어 있어야 합니다. 오른쪽 위에 내 프로필 사진이 보이면 로그인된 상태입니다.
- 브라우저 탭 하나만 있으면 됩니다. 설치할 프로그램은 없습니다.
- 이 실습에서 만드는 `lunch-practice`는 1교시부터 4교시, 그리고 7교시까지 계속 씁니다. **오늘 수업이 끝날 때까지 지우지 마세요.**

## STEP 1. Starter 템플릿 열기

강사가 준비한 Starter 리포지토리는 **템플릿**(template)으로 설정되어 있습니다. 템플릿은 "이 리포지토리를 본떠서 내 리포지토리를 새로 만들 수 있다"는 뜻입니다.

1. 브라우저 주소창에 아래 주소를 입력하고 ++enter++ 를 누릅니다.

    ```text
    https://github.com/skilleat-labs/lunch-picker-starter
    ```

2. 화면 위쪽에 `skilleat-labs / lunch-picker-starter`라는 이름과 **Public template**이라는 표시가 보이는지 확인합니다.
3. 파일 목록에 `.github`, `docs`, `scripts`, `site`, `README.md`가 보이는지 확인합니다.

확인: 화면 오른쪽 위, 파일 목록 위쪽에 초록색 **Use this template**(이 템플릿 사용) 버튼이 보입니다.

## STEP 2. 템플릿으로 내 리포지토리 만들기

1. 초록색 **Use this template** 버튼을 클릭합니다.
2. 펼쳐진 메뉴에서 **Create a new repository**(새 리포지토리 만들기)를 클릭합니다.
3. "Create a new repository" 화면이 열립니다. 아래 표대로 입력합니다.

    | 항목 | 입력하거나 고를 값 | 설명 |
    |---|---|---|
    | **Include all branches** | 체크하지 않음 (기본값 그대로) | 템플릿의 main 분기만 가져옵니다 |
    | **Owner** | 내 GitHub 아이디 | 드롭다운을 눌러 내 아이디를 고릅니다. 조직 이름이 보여도 고르지 않습니다 |
    | **Repository name** | `lunch-practice` | 아래 코드 블록을 복사해서 붙여 넣으세요 |
    | **Description** | 비워 둠 | 선택 항목입니다 |
    | 공개 범위 | **Public** | 오늘 실습은 모두 공개 리포지토리로 합니다 |

    ```text
    lunch-practice
    ```

4. Repository name 칸 아래에 초록색 체크 표시와 함께 `lunch-practice is available.`이 보이는지 확인합니다.
5. 화면 맨 아래 초록색 **Create repository**(리포지토리 만들기) 버튼을 클릭합니다.
6. 몇 초 동안 "Generating your repository..." 화면이 보였다가 새 리포지토리로 이동합니다.

확인: 화면 위쪽에 `내아이디 / lunch-practice`가 보이고, 그 아래에 작은 글씨로 `generated from skilleat-labs/lunch-picker-starter`가 보입니다.

!!! note "왜 Public으로 만드나요?"
    오늘 쓰는 무료(Free) 요금제에서는 공개 리포지토리여야 GitHub Pages 웹페이지, 분기 보호 같은 기능을 모두 쓸 수 있습니다. 실습 파일에는 개인 정보가 없으니 공개해도 괜찮습니다. 회사 업무 리포지토리는 회사 규정에 따라 Private(비공개)로 만듭니다.

## STEP 3. 만들어진 리포지토리 둘러보기

방금 만든 리포지토리의 첫 화면(**Code** 탭)을 위에서 아래로 훑어봅니다.

1. **주소 확인**: 브라우저 주소창을 봅니다. 주소는 이런 구조입니다.

    ```text
    https://github.com/<내아이디>/lunch-practice
    ```

    `github.com` 다음이 **주인(Owner)**, 그다음이 **리포지토리 이름**입니다. 짝꿍이나 강사에게 내 리포지토리를 알려 줄 때 이 주소를 그대로 복사해서 주면 됩니다.

2. **탭 확인**: 리포지토리 이름 아래에 **Code**, **Issues**, **Pull requests**, **Actions**, **Projects**, **Settings** 등의 탭이 있습니다. 지금은 **Code** 탭이 선택되어 있습니다.

3. **파일 목록 확인**: 가운데 파일 목록에 아래 항목이 보입니다.

    | 이름 | 무엇인가 |
    |---|---|
    | `.github` | 자동 작업(Actions) 설정이 들어 있는 폴더 |
    | `docs` | 현업 요청, 킥오프 회의록, 현행 업무 문서 |
    | `scripts` | 메뉴 데이터를 검사하는 프로그램 |
    | `site` | 점심 메뉴 추천 웹페이지 (`index.html`, `menus.json`) |
    | `README.md` | 리포지토리 소개 문서 |

4. **README 확인**: 파일 목록 아래로 스크롤하면 `README.md`의 내용이 자동으로 펼쳐져 보입니다. 지금은 "점심 메뉴 추천 서비스"라는 제목과 한 줄 소개뿐입니다. 2교시에 이 README를 꾸밉니다.

5. **커밋 수 확인**: 파일 목록 바로 위 회색 줄을 봅니다. 왼쪽에는 내 아이디와 `Initial commit`이라는 메시지가, 오른쪽 끝에는 시계 아이콘과 함께 **1 Commit**이 보입니다.

확인: 커밋 수가 **1 Commit**입니다. 템플릿으로 만들면 Starter의 이력은 따라오지 않고, 지금 상태의 파일이 담긴 커밋 1개로 새로 시작합니다.

!!! note "템플릿으로 만들기와 Fork는 무엇이 다른가요?"
    다른 사람의 리포지토리를 내 계정으로 가져오는 방법은 두 가지입니다.

    | 구분 | Use this template (템플릿 복사) | Fork (갈래 복사) |
    |---|---|---|
    | 이력 | 커밋 1개로 **새로 시작** | 원본의 커밋 이력을 **모두 가져옴** |
    | 원본과의 관계 | 끊어짐. 완전히 독립된 내 리포지토리 | 이어짐. 원본에 Pull Request로 변경을 제안할 수 있음 |
    | 리포지토리 이름 | 원하는 이름으로 지정 | 기본으로 원본과 같은 이름 |
    | 주로 쓰는 경우 | 양식을 본떠 새 프로젝트 시작 | 오픈소스 같은 남의 프로젝트에 기여 |

    오늘은 Starter를 출발점으로 삼아 각자 독립된 프로젝트를 만드는 것이므로 템플릿 복사를 씁니다.

## STEP 4. 첫 배포가 실패한 것 확인하기

Starter에는 `main`에 커밋이 생기면 `site/` 폴더를 웹페이지로 배포하는 자동 작업(**웹페이지 배포**)이 들어 있습니다. 리포지토리를 만드는 순간 첫 커밋이 생겼으니 이 작업이 이미 한 번 실행되었습니다. 그런데 **실패했을 겁니다.** 정상입니다.

1. 리포지토리 위쪽 탭에서 **Actions**를 클릭합니다.
2. 목록에 `Initial commit`이라는 실행 기록이 있고, 왼쪽에 빨간 X 표시가 있는지 봅니다. (아직 돌고 있으면 노란 원이 돕니다. 잠시 기다립니다.)

확인: 빨간 X가 보입니다. 눌러 보면 `Get Pages site failed` 비슷한 오류가 보입니다.

!!! note "왜 첫 배포는 실패하나요?"
    템플릿으로 만든 리포지토리에는 Pages(웹페이지 호스팅) 설정이 따라오지 않습니다. Pages가 꺼진 상태에서 배포를 시도했으니 "Pages 사이트를 찾을 수 없다"는 오류로 실패한 것입니다. 다음 STEP에서 Pages를 켜고 다시 실행하면 성공합니다.

## STEP 5. GitHub Pages 켜기

**GitHub Pages**는 리포지토리의 파일로 웹사이트를 무료로 열어 주는 기능입니다.

1. 리포지토리 위쪽 탭에서 **Settings**(설정)를 클릭합니다. 탭이 안 보이면 탭 줄 오른쪽 끝의 **...** 을 눌러 찾습니다.
2. 왼쪽 메뉴를 아래로 내려 **Code and automation** 묶음 아래의 **Pages**를 클릭합니다.
3. **Build and deployment** 영역의 **Source** 드롭다운을 봅니다. 지금은 `Deploy from a branch`로 되어 있습니다.
4. **Source** 드롭다운을 클릭하고 **GitHub Actions**를 고릅니다.
5. 따로 저장 버튼은 없습니다. 고르는 즉시 저장됩니다.

확인: **Source**가 `GitHub Actions`로 바뀌어 있습니다.

!!! warning "Use a suggested workflow, Configure 버튼은 누르지 않습니다"
    Source를 GitHub Actions로 바꾸면 아래에 Jekyll, Static HTML 같은 추천 작업 카드와 **Configure** 버튼이 나올 수 있습니다. 우리 리포지토리에는 이미 배포 작업(`.github/workflows/pages.yml`)이 있으므로 아무것도 누르지 않습니다.

## STEP 6. 배포 작업 직접 실행하기

Pages를 켰으니 배포 작업을 한 번 더 실행합니다.

1. 리포지토리 위쪽 탭에서 **Actions**를 클릭합니다.
2. 왼쪽 **All workflows** 아래 목록에서 **웹페이지 배포**를 클릭합니다.
3. 오른쪽에 `This workflow has a workflow_dispatch event trigger.`라는 안내와 함께 **Run workflow** 버튼이 보입니다. **Run workflow**를 클릭합니다.
4. 작은 창이 펼쳐집니다. **Use workflow from**이 `Branch: main`인지 확인합니다.
5. 펼쳐진 창 안의 초록색 **Run workflow** 버튼을 클릭합니다.
6. 몇 초 뒤 목록 맨 위에 새 실행 기록이 노란 원(실행 중)으로 나타납니다. 나타나지 않으면 브라우저를 새로고침합니다.
7. 1~2분 기다리면 노란 원이 초록 체크로 바뀝니다.

확인: 새 실행 기록 왼쪽에 **초록 체크**가 보입니다.

## STEP 7. 웹페이지 열기

1. 리포지토리 위쪽 탭에서 **Settings**를 클릭하고, 왼쪽 메뉴에서 **Pages**를 클릭합니다.
2. 화면 위쪽에 `Your site is live at`라는 문구와 함께 주소가 보입니다. 주소는 이런 모양입니다.

    ```text
    https://<내아이디>.github.io/lunch-practice/
    ```

3. 주소 옆의 **Visit site** 버튼을 클릭합니다. (새 탭에서 열립니다.)
4. "점심 메뉴 추천" 웹페이지가 열립니다. 아래 내용을 하나씩 확인합니다.
    - 파란 머리말에 `점심 메뉴 추천`, `오늘 점심, 5분 안에 정해 봅시다.`
    - 예산(원), 거리(m) 입력칸과 **아무거나 골라 줘** 버튼
    - 메뉴 카드 **6개**: 김치찌개, 짜장면, 돈카츠, 샐러드볼, 쌀국수, 순두부찌개
    - 김치찌개, 샐러드볼, 순두부찌개 카드에는 `혼밥 가능` 배지
5. 예산 칸에 `9000`을 입력해 봅니다. 9,000원 이하 메뉴(김치찌개, 짜장면, 순두부찌개)만 남는지 확인합니다.
6. **아무거나 골라 줘** 버튼을 눌러 "오늘의 추천: ..." 문구가 나오는지 확인합니다.

확인: 메뉴 카드 6개가 보이는 웹페이지가 열립니다. 이 주소를 브라우저 즐겨찾기에 넣어 두세요. 실습 1-2에서 다시 엽니다.

!!! note "웹페이지 내용은 어디서 오나요?"
    이 웹페이지는 리포지토리의 `site/index.html`이 화면 모양을, `site/menus.json`이 메뉴 데이터를 담당합니다. 다음 실습에서 `menus.json`의 가격을 고치고 커밋하면, 배포 작업이 자동으로 다시 돌아서 웹페이지에도 반영됩니다.

## 성공하면

- [x] `https://github.com/<내아이디>/lunch-practice` 리포지토리가 있습니다. Public입니다.
- [x] 첫 화면에 **1 Commit**, 파일 목록, README가 보입니다.
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

??? failure "Run workflow를 눌렀는데 또 빨간 X입니다"
    **Settings** → **Pages**의 Source가 `GitHub Actions`로 바뀌었는지 다시 확인합니다. 바뀌어 있다면 빨간 X 실행 기록을 클릭하고, 오른쪽 위 **Re-run jobs** → **Re-run all jobs**를 눌러 한 번 더 실행합니다.

??? failure "Pages 화면에 주소가 안 보이거나, 주소를 열면 404가 나옵니다"
    배포가 끝난 지 얼마 안 되면 1~2분 정도 404가 보일 수 있습니다. 잠시 기다린 뒤 새로고침합니다. 그래도 안 되면 **Actions** 탭에서 **웹페이지 배포** 최신 실행이 초록 체크인지 확인합니다. 초록 체크인 실행을 클릭하면 `deploy` 상자 아래에도 웹페이지 주소가 보입니다.

## 다음 실습으로 넘어가기 전에

- `lunch-practice` 리포지토리 탭과 웹페이지 탭을 둘 다 열어 둡니다.
- 리포지토리는 오늘 끝까지 씁니다. 지우거나 이름을 바꾸지 않습니다.
