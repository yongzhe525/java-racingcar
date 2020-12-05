# 자동차 경주 게임
## 진행 방법
* 자동차 경주 게임 요구사항을 파악한다.
* 요구사항에 대한 구현을 완료한 후 자신의 github 아이디에 해당하는 브랜치에 Pull Request(이하 PR)를 통해 코드 리뷰 요청을 한다.
* 코드 리뷰 피드백에 대한 개선 작업을 하고 다시 PUSH한다.
* 모든 피드백을 완료하면 다음 단계를 도전하고 앞의 과정을 반복한다.

## 온라인 코드 리뷰 과정
* [텍스트와 이미지로 살펴보는 온라인 코드 리뷰 과정](https://github.com/next-step/nextstep-docs/tree/master/codereview)

# 문자열 계산기
## 기능 요구사항
* 사용자가 입력한 문자열 값에 따라 사칙연산을 수행할 수 있는 계산기를 구현해야 한다.
* 입력 문자열의 숫자와 사칙 연산 사이에는 반드시 빈 공백 문자열이 있다고 가정한다.
* 나눗셈의 경우 결과 값을 정수로 떨어지는 값으로 한정한다.
* 문자열 계산기는 사칙연산의 계산 우선순위가 아닌 입력 값에 따라 계산 순서가 결정된다. 즉, 수학에서는 곱셈, 나눗셈이 덧셈, 뺄셈 보다 먼저 계산해야 하지만 이를 무시한다.
* 예를 들어 2 + 3 * 4 / 2와 같은 문자열을 입력할 경우 2 + 3 * 4 / 2 실행 결과인 10을 출력해야 한다.

## 프로그래밍 요구사항
* 메소드가 너무 많은 일을 하지 않도록 분리하기 위해 노력해 본다.

## To do
 - [X] 입력값 파싱:: InputValid 클래스를 상속받는 Numbers, Operators 클래스(일급객체) 구현
    - [X] null이거나 빈 공백 문자일 경우 IllegalArgumentException throw
    - [X] 숫자(정수)로 변환 불가능한 값의 경우 IllegalArgumentException throw
    - [X] 들어온 순번에 맞는 숫자를 반환
    - [X] 들어온 순번에 맞는 연산자를 반환
- [X] 입력 문자열의 연산 처리 :: Enum 사용해보기
    - [X] 덧셈
    - [X] 뺄셈
    - [X] 곱셈
    - [X] 나눗셈
        - [X] 결과 값은 정수로 떨어지는 값으로 한정
        - [X] 0으로 나눌경우 IllegalArgumentException throw
 - [X] 사칙 연산을 모두 포함하는 기능 구현 :: Calculator 클래스 구현
    - [X] 사칙 연산 수행