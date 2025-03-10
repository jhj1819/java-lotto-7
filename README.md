# java-lotto-precourse

# 구현할 기능 정보

1. 구매 금액 입력받기
   - 사용자로부터 구매할 금액을 입력받는다.
2. 로또 번호 자동 생성기 구현
   - 1~45까지의 숫자 중 6개를 랜덤으로 생성한다.
3. 구매 금액만큼 로또 자동 생성
   - 입력받은 금액만큼 로또를 생성한다.
4. 당첨/보너스 번호 입력받기
   - 사용자로부터 당첨 번호 6개와 보너스 번호 1개를 입력받는다
5. 뽑은 번호 출력
6. 당첨조회/수익률계산 구현
   - 등수별 당첨 개수를 저장하는 LottoResult 클래스 구현
   - 당첨번호와 구매한 로또 번호를 비교하여 당첨 여부 계산 클래스 구현
   - 당첨 결과를 추가하고, 총 상금을 계산하는 메서드 구현
   - 당첨 등수와 상금을 관리하는 Rank 열거형 추가
   - 당첨 결과를 출력하는 printResult 메서드 구현
   - 총 당첨 금액과 구매 금액을 이용하여 수익률을 계산하고 출력하는 기능 구현

- 예외처리
  - 사용자가 잘못된 값을 입력할 경우 IllegalArgumentException을 발생시키고 "[ERROR]"로 시작하는 에러 메시지를 출력 후 종료
    - 구매 금액 예외 처리
      - 숫자가 아닌 값
      - 1000원으로 나눠 떨어지지 않는 값
      - 0원 또는 음수값
    - 당첨/보너스 번호 예외 처리
      - 숫자가 아닌 값
      - 1~45 범위를 벗어나는 값
      - 중복된 값
      - 당첨 번호가 6개가 아닌 경우
      - 보너스 번호가 1개가 아닌 경우
  - 에러 메세지 출력 후 종료하지 않고 그 부분부터 입력을 다시 받는다.
  - Exception이 아닌 IllegalArgumentException, IllegalStateException 등과 같은 명확한 유형을 처리한다.

- 리팩토링

- 순서 다이어그램(활동막대 생략
![CodeRabbit Pull Request Reviews](https://img.shields.io/coderabbit/prs/github/jhj1819/java-racingcar-7?labelColor=171717&color=FF570A&link=https%3A%2F%2Fcoderabbit.ai&label=CodeRabbit%20Reviews)