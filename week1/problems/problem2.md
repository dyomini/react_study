# 항공편 예약하기

> 항공편을 예약하는 데 필요한 정보를 입력하는 기능을 구현합니다.
> 단, 지문 및 초기 코드로 제공된 선택자가 다를 경우 정상적으로 채점이 되지 않을 수 있습니다.

## ✅ 2.1 탑승객 정보 입력하기

<img src="./images/q2_1.gif" width="50%" height="50%">

- 항공편의 탑승객 인원 수에 맞게 탑승객 정보 입력칸이 동적으로 생성됩니다.

  - 예를 들어, 선택된 탑승객 인원 수가 성인 1명, 소아 1명으로 총 2명인 경우, 2개의 입력칸이 생성됩니다. 위의 예시 GIF를 참고해 주세요.

- 탑승객 정보 입력칸은 아래 4가지 요소로 구성되어 있습니다.
  - `영문 이름`
  - `영문 성`
  - `생년월일`
  - `여권번호`
- 각 요소의 입력 조건은 다음과 같습니다.
  - `영문 이름`과 `영문 성`
    - 해당 입력칸에 소문자를 입력하면 키가 입력되는 시점에 자동으로 대문자로 변환되어 입력됩니다.
  - `생년월일`
    - 총 8자리이며, `YYYY.MM.DD.` 형식으로 입력 가능합니다.
    - 해당 입력칸에 숫자를 입력하면 키가 입력되는 시점에 년도, 월, 일 단위로 기호 `.`가 입력됩니다.
    - 8자리의 생년월일 입력 후, `여권번호` 입력 칸으로 자동으로 탭 이동이 이루어집니다.
  - `여권번호`
    - 총 9자리이며, 영대문자 1자리 + 숫자 8자리 형식으로 입력 가능합니다.
    - 숫자 8자리의 경우, 연속된 숫자 2자리 이상 입력할 수 없습니다. (오름차순인 경우에 대해서만 확인이 이루어집니다.)
    - 9자리를 모두 입력한 시점에 유효성 검사가 이루어집니다.
      - 입력된 여권번호의 형식이 올바르지 않은 경우 `알맞은 여권 번호 형식이 아닙니다.` 문구의 다이얼로그 창(`window.alert`)이 나타납니다.
      - 올바른 형식의 여권번호르 입력하였으나 연속된 2자리의 숫자가 포함된 경우 `연속된 2자리 이상의 숫자는 사용할 수 없습니다.` 문구의 다이얼로그 창(`window.alert`)이 나타납니다.
      - 위 두가지의 다이얼로그 창을 닫으면 `여권번호` 입력칸은 초기화됩니다.

## ✅ 2.2. 항공료 계산하기

<img src="./images/q2_2.gif" width="50%" height="50%">

### 2.2.1 기본 항공료 계산하기

- 성인과 소아의 1인당 금액은 아래와 같습니다.
  |탑승객|항공료|
  | :--: | :--: |
  | 성인 | 55,000원 |
  | 소아 | 성인 항공료의 10% |

- 선택되는 성인과 소아의 인원 수에 따라 총액 계산이 이루어집니다.
- 항공료 금액의 기본 단위는 `₩(KRW)`으로 설정되어 있으며, 천원 단위로 쉼표(`,`) 기호가 표시됩니다.

### 2.2.2 화폐 단위 변경하기

- 항공료 금액의 경우, 아래 총 3가지에 대해서 화폐 단위를 변경할 수 있습니다.

  - `원화`
  - `엔화`
  - `달러`

- `엔화`와 `달러`의 환율 가격은 아래와 같습니다.
  |단위|환율|
  | :--: | :--: |
  | 엔화 | 1,022/100엔 |
  | 달러 | 1,235/달러 |

  (\* 환율 계산 시 소수점은 버립니다.)

- 화폐 단위를 변경하는 경우, 금액과 화폐 단위가 함께 바뀝니다. 예시 GIF를 참고해 주세요.

### 2.2.3 할인 코드 적용하기

- 할인코드를 통해 항공료 할인을 받을 수 있으며, 총 3가지 종류의 할인 코드가 있습니다. 각 할인 코드에 대한 할인율은 다음과 같습니다.
  |할인코드|할인율|
  | :--: | :--: |
  | `AD` | 성인 가격의 3% |
  | `CH` | 소아 가격의 2% |
  | `AL` | 전체 가격의 8% |
- 할인코드의 입력 조건은 다음과 같습니다.
  - 영대문자 2자리 + 숫자 4자리의 형식입니다.
  - 성인이 탑승하는 경우에는 `AD` 영문 코드를 사용할 수 있습니다.
  - 소아가 탑승하는 경우에는 `CH` 영문 코드를 사용할 수 있습니다.
  - 성인과 소아가 모두 탑승할 경우에는 `AL` 영문 코드를 사용할 수 있습니다.
