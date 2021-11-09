# 로또
## 진행 방법
* 로또 요구사항을 파악한다.
* 요구사항에 대한 구현을 완료한 후 자신의 github 아이디에 해당하는 브랜치에 Pull Request(이하 PR)를 통해 코드 리뷰 요청을 한다.
* 코드 리뷰 피드백에 대한 개선 작업을 하고 다시 PUSH한다.
* 모든 피드백을 완료하면 다음 단계를 도전하고 앞의 과정을 반복한다.

## 온라인 코드 리뷰 과정
* [텍스트와 이미지로 살펴보는 온라인 코드 리뷰 과정](https://github.com/next-step/nextstep-docs/tree/master/codereview)

***
### 요구사항
* 로또 구입 금액을 입력받는다.
* 구입 금액에 해당하는 로또를 발급한다.
    * 로또 1장의 가격은 1000원이다.
* 구입한 로또의 개수를 출력한다.
* 구입한 로또의 번호를 모두 출력한다.
    * 각 로또 번호는 오름차순으로 출력한다.
* 지난 주 당첨 번호를 입력 받는다.
* 지난 주 번호를 기준으로 당첨을 확인한다.
* 당첨 확인 결과를 통계로 출력한다.
    * 번호가 3개 ~ 6개 일치하는 항목의 개수를 출력한다.
    * 일치하는 개수 출력 시 당첨 금액이 함께 표시되어야 한다.
    * 총 수익률을 소수점 2자리의 정수 형태로 출력한다.

### 기능 목록
- [x] 로또 번호
    - [x] 번호의 범위 (1 이상 45 이하) 유효성 검사
    - [x] 범위를 벗어날 경우 예외 발생
- [x] 로또
  - [x] 6개의 번호가 아닌 경우 예외 발생
  - [x] 중복된 번호가 있으면 예외 발생
  - [x] 다른 로또와 일치하는 번호의 개수 확인
  - [x] 하나의 번호가 존재하는지 확인
- [x] 로또 생성
  - [x] 6개의 랜덤한 번호를 생성
  - [x] 이전과 완벽하게 동일한 번호의 로또를 생성하지 않음
- [x] Money
  - [x] 0 이상인지 유효성 검사
  - [x] 구입한 금액만큼 차감
  - [x] 과소비 허용 안 함
- [x] 로또 판매점
    - [x] 구입 금액 확인
    - [x] 금액 범위 내에서 최대한 로또를 발급
- [x] Rank(당첨 등수)
  - [x] 일치하는 번호 개수를 전달받아 Rank로 변환
  - [x] 2등 당첨 확인 기능 추가
- [x] 통계
    - [x] 수익률 계산
    - [x] 당첨 등수별 개수 제공 
- [x] 로또 목록(Lottos)
  - [x] 로또의 개수 반환
  - [x] 목록 반환
  - [x] null or Empty 시 예외 발생
- [x] 당첨 번호 (WinningLotto)
  - [x] 당첨 로또 번호
  - [x] 보너스 볼 번호
  - [x] 당첨 번호에 보너스 볼 번호가 포함되어 있으면 예외 
- [x] 입력
  - [x] 구입 금액 입력
  - [x] 지난주 당첨 번호 입력
  - [x] 보너스 볼 입력
- [x] 출력
  - [x] 구입한 로또 개수 출력
  - [x] 구입한 로또 번호 출력
  - [x] 통계 출력 기능
    - [x] 등수 별 당첨 금액, 당첨 개수 출력
    - [x] 수익률 출력