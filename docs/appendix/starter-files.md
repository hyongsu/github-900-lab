# Starter 파일 보기

모든 실습은 강사가 준비한 Starter Repository에서 시작합니다. **Use this template** 버튼으로 내 계정에 복사해서 씁니다.

- 주소: [https://github.com/skilleat-labs/lunch-picker-starter](https://github.com/skilleat-labs/lunch-picker-starter)

```text
lunch-picker-starter/
├── README.md                     서비스 한 줄 소개
├── docs/
│   ├── 00_현업요청.md             경영지원팀의 요청 메일
│   ├── 01_킥오프_회의록.md        킥오프 회의 기록 (결정하지 못한 것 포함)
│   ├── 02_현행_업무.md            지금 메뉴를 정하는 방식
│   └── images/lunch.svg           README에 넣는 그림
├── site/
│   ├── index.html                 점심 메뉴 웹페이지
│   └── menus.json                 메뉴 데이터
├── scripts/
│   └── check-menus.js             메뉴 데이터 검사 프로그램
└── .github/workflows/
    ├── check.yml                  PR이 열리면 메뉴 데이터 검사
    └── pages.yml                  main에 반영되면 웹페이지 배포
```

## 요구사항 원재료

??? note "docs/00_현업요청.md"
    ```markdown
    --8<-- "starter/docs/00_현업요청.md"
    ```

??? note "docs/01_킥오프_회의록.md"
    ```markdown
    --8<-- "starter/docs/01_킥오프_회의록.md"
    ```

??? note "docs/02_현행_업무.md"
    ```markdown
    --8<-- "starter/docs/02_현행_업무.md"
    ```

## 웹페이지

메뉴 데이터 한 줄의 항목은 아래와 같습니다.

| 항목 | 뜻 | 형식 | 예 |
|---|---|---|---|
| `name` | 메뉴 이름 | 글자 (따옴표) | `"김치찌개"` |
| `category` | 종류 | 글자 (따옴표) | `"한식"` |
| `price` | 가격 (원) | 숫자 (따옴표 없음) | `9000` |
| `distance` | 회사에서 거리 (미터) | 숫자 (따옴표 없음) | `300` |
| `solo` | 혼밥 가능 | `true` 또는 `false` | `true` |
| `delivery` | 배달 가능 (6교시에 추가) | `true` 또는 `false` | `false` |

```json title="site/menus.json"
--8<-- "starter/site/menus.json"
```

??? note "site/index.html"
    ```html
    --8<-- "starter/site/index.html"
    ```

## 자동화

```yaml title=".github/workflows/check.yml"
--8<-- "starter/.github/workflows/check.yml"
```

```yaml title=".github/workflows/pages.yml"
--8<-- "starter/.github/workflows/pages.yml"
```

??? note "scripts/check-menus.js"
    ```javascript
    --8<-- "starter/scripts/check-menus.js"
    ```
