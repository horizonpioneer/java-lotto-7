# java-lotto-precourse


#### 📌기능 요구 사항에 기재되지 않은 내용이지만 개인 판단 하에 구현한 내용에는 💡를 남겼습니다.

## 로또

로또 발매기를 구현하여, 구매한 로또 번호와 당첨 번호를 비교해 당첨 내역과 수익률을 계산해 도출하는 로또 게임

## 기능 요구 사항

- 로또 번호의 숫자 범위는 1~45까지이다.
- 1개의 로또를 발행할 때 중복되지 않는 6개의 숫자를 뽑는다.
- 당첨 번호 추첨 시 중복되지 않는 숫자 6개와 보너스 번호 1개를 뽑는다.
- 당첨은 1등부터 5등까지 있다. 당첨 기준과 금액은 아래와 같다.
    - 1등: 6개 번호 일치 / 2,000,000,000원
    - 2등: 5개 번호 + 보너스 번호 일치 / 30,000,000원
    - 3등: 5개 번호 일치 / 1,500,000원
    - 4등: 4개 번호 일치 / 50,000원
    - 5등: 3개 번호 일치 / 5,000원


- 로또 구입 금액을 입력하면 구입 금액에 해당하는 만큼 로또를 발행해야 한다.
- 로또 1장의 가격은 1,000원이다.
- 당첨 번호와 보너스 번호를 입력받는다.
- 사용자가 구매한 로또 번호와 당첨 번호를 비교하여 당첨 내역 및 수익률을 출력하고 로또 게임을 종료한다.
- 사용자가 잘못된 값을 입력할 경우 'IllegalArgumentException'을 발생시키고, "[ERROR]"로 시작하는 에러 메시지를 출력 후 그 부분부터 입력을 다시 받는다.
    - 'Exception'이 아닌 'IllegalArgumentException', 'IllegalStateException' 등과 같은 명확한 유형을 처리한다.

---
## 기능 구현 목록


- 로또 번호 발행기
    - [ ] 1개의 로또를 발행할 때 중복되지 않는 6개의 숫자를 뽑는다.


- 로또
    - [ ] 사용자가 구매한 로또 번호와 당첨 번호를 비교하여 번호 일치 개수를 확인한다.
    - [ ] 사용자가 구매한 로또 번호에 보너스 번호와 일치하는 번호가 있는지 확인한다.


- 로또 결과
    - [ ] 번호 일치 개수를 통해 당첨 금액을 계산한다.
    - [ ] 수익률을 계산한다.
        - [ ]  수익률을 소수점 둘째 자리에서 반올림한다.


- 입력
    - [x] 로또 구입 금액을 입력 받는다.
    - [x] 당첨 번호를 입력받는다. (번호는 쉼표(,)로 구분한다.)
    - [x] 보너스 번호를 입력받는다.


- 입력값 분리
    - [ ] 입력 받은 당첨 번호를 쉼표(,)를 기준으로 분리한다.


- 출력
    - [ ] 발행한 로또 수량을 출력한다.
    - [ ] 발행한 로또 번호를 출력한다.
        - [ ] 발행한 로또 번호를 오름차순으로 정렬한다.
    - [ ] 당첨 내역을 출력한다.
    - [ ] 수익률을 출력한다.
    - [x] 예외 상황 시 에러 문구를 출력한다. ("[ERROR]" + 에러 문구)


- 예외
    - [x] 입력값이 빈 문자열이거나 공백문자로만 이루어진 경우, 예외를 발생시킨다. 💡
    - [x] 입력 받은 로또 구입 금액이 1000으로 나누어 떨어지지 않는 경우, 예외를 발생시킨다.
    - [ ] 입력 받은 당첨 번호가 1~45 범위의 숫자가 아닌 경우, 예외를 발생시킨다.
    - [ ] 입력 받은 당첨 번호가 6개가 아닌 경우, 예외를 발생시킨다.
    - [x] 입력 받은 당첨 번호가 쉼표로 구분되지 않을 경우, 예외를 발생시킨다.
    - [x] 입력 받은 보너스 번호가 1~45 범위의 숫자가 아닌 경우, 예외를 발생시킨다.
    - [ ] 입력 받은 보너스 번호가 입력 받은 당첨 번호 중 하나와 중복되는 경우, 예외를 발생시킨다.
