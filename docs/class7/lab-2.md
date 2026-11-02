# 실습 7-2. 2단계 인증 켜기

!!! abstract "이번 실습에서 할 것"
    - 내 GitHub 계정에 2단계 인증(2FA)을 켭니다.
    - 휴대폰 인증 앱을 연결하고, 복구 코드를 안전한 곳에 보관합니다.

**소요 시간** 약 4분  **실습 장소** 내 GitHub 계정 설정 (리포지토리가 아닙니다)  **관련 교안** [인증 방식 네 가지](index.md#auth)

## 준비

- 휴대폰에 인증 앱이 있어야 합니다. Google Authenticator, Microsoft Authenticator 등 아무것이나 됩니다. 없으면 앱 스토어에서 설치합니다.
- 이미 2단계 인증이 켜져 있는 분은 STEP 1에서 상태만 확인하고 끝냅니다.
- 시간이 부족하면 이 실습은 **교육 후 과제**로 해도 됩니다. 다만 꼭 하세요. GitHub는 코드를 올리는 계정에 2단계 인증을 의무로 요구하고 있습니다.

!!! warning "회사 보안 규정을 먼저 따르세요"
    회사 계정(SAML SSO로 로그인하는 계정)이거나 회사가 정한 인증 앱이 있으면 그 규정을 따릅니다. 이 실습은 오늘 쓴 개인 GitHub 계정 기준입니다.

## STEP 1. 2단계 인증 설정 화면 열기

1. GitHub 오른쪽 위 내 프로필 사진 클릭 → **Settings**(설정) 클릭
2. 왼쪽 **Access** 아래 **Password and authentication**(비밀번호와 인증) 클릭
3. **Two-factor authentication**(2단계 인증) 영역을 봅니다.
    - **Enable two-factor authentication**(2단계 인증 켜기) 버튼이 보이면 아직 꺼져 있는 것입니다. STEP 2로 갑니다.
    - **Enabled**(켜짐) 표시가 보이면 이미 켜져 있습니다. 아래 [이미 켜져 있다면](#already-enabled)으로 갑니다.

확인: 2단계 인증이 켜져 있는지 꺼져 있는지 알 수 있습니다.

## STEP 2. 인증 앱 연결하기

1. **Enable two-factor authentication** 클릭. 비밀번호나 메일 인증을 다시 물으면 입력합니다.
2. 화면에 QR 코드가 나옵니다.
3. 휴대폰 인증 앱을 열고 **+**(추가) → **QR 코드 스캔** → 화면의 QR 코드를 비춥니다.
4. 앱에 `GitHub` 항목과 30초마다 바뀌는 6자리 숫자가 생깁니다.
5. GitHub 화면의 **Verify the code from the app**(앱의 코드 입력) 칸에 6자리 숫자를 입력합니다. 숫자가 바뀌기 직전이면 다음 숫자를 기다렸다 입력하세요.
6. **Continue**(계속) 클릭

확인: 다음 화면에 **Save your recovery codes**(복구 코드 저장)가 나옵니다.

## STEP 3. 복구 코드 보관하기

**Recovery codes**(복구 코드)는 휴대폰을 잃어버렸을 때 로그인할 수 있는 일회용 비상 열쇠입니다. 16개 정도의 코드가 나오고, 하나에 한 번씩 쓸 수 있습니다.

1. **Download**(내려받기) 클릭해 파일로 저장하거나, **Copy**(복사) 클릭해 안전한 곳에 붙여 넣습니다.
2. 보관 장소는 회사 보안 규정에 맞게 고릅니다. 예: 회사가 허용한 비밀번호 관리자, 인쇄해서 잠금 서랍. 메신저, 메일, 공유 문서, GitHub 리포지토리에는 **절대 두지 않습니다.**
3. **I have saved my recovery codes**(복구 코드를 저장했습니다) 클릭
4. 마지막 화면에서 **Done**(완료) 클릭

!!! danger "복구 코드를 잃어버리면"
    휴대폰과 복구 코드를 둘 다 잃어버리면 GitHub 지원팀도 계정을 복구해 줄 수 없습니다. 오늘 만든 리포지토리를 모두 잃게 됩니다. 지금 바로 저장하세요.

확인: **Password and authentication** 화면의 Two-factor authentication에 **Enabled**가 보이고, Authenticator app이 Configured(설정됨)로 나옵니다.

## 이미 켜져 있다면 { #already-enabled }

1. **Two-factor authentication** 영역의 **Recovery options**(복구 수단)에서 **Recovery codes** → **View**(보기)를 눌러 복구 코드가 아직 있는지, 어디에 보관했는지 확인합니다.
2. 보관한 곳이 기억나지 않으면 **Regenerate**(다시 만들기)로 새 코드를 받아 STEP 3처럼 보관합니다. 예전 코드는 쓸 수 없게 됩니다.

## 성공하면

- [x] **Settings** → **Password and authentication**에서 Two-factor authentication이 **Enabled**다
- [x] 휴대폰 인증 앱에 GitHub 6자리 코드가 보인다
- [x] 복구 코드를 회사 규정에 맞는 안전한 곳에 보관했다

## 막히면

??? failure "6자리 코드를 넣었는데 틀렸다고 나와요"
    휴대폰 시간이 실제 시간과 다르면 코드가 맞지 않습니다. 휴대폰 설정에서 날짜와 시간을 **자동**으로 바꾼 뒤 다시 입력하세요. 숫자가 바뀌기 직전에 넣었다면 새 숫자로 다시 해 봅니다.

??? failure "QR 코드가 스캔되지 않아요"
    QR 코드 아래 **setup key**(설정 키) 링크를 누르면 긴 문자열이 나옵니다. 인증 앱에서 **설정 키 입력**(Enter a setup key)을 골라 계정 이름 `GitHub`, 키에 그 문자열을 넣습니다.

??? failure "인증 앱을 설치할 수 없어요 (회사 휴대폰 정책 등)"
    오늘은 건너뛰고 교육 후 과제로 합니다. 인증 앱 대신 GitHub Mobile 앱이나 보안 키(Passkey)도 쓸 수 있습니다. 회사 IT 담당 부서에 허용된 방법을 확인하세요.

??? failure "2단계 인증을 켠 뒤 다른 곳에서 로그인이 안 돼요"
    로그인할 때 비밀번호 다음에 인증 앱의 6자리 코드를 입력해야 합니다. 휴대폰이 없으면 **Use a recovery code**(복구 코드 사용)를 누르고 보관한 코드 하나를 입력합니다.

## 다음으로 넘어가기 전에

- 휴대폰을 바꿀 때는 인증 앱 계정을 새 휴대폰으로 옮긴 뒤 예전 휴대폰을 초기화하세요.
- 마지막 [오늘의 정리](wrap-up.md)로 넘어갑니다.
