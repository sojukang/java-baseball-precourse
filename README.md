# 미션 - 숫자 야구 게임

## 기능 구현 목록

### 세 자리 난수 생성

- Random 값 추출은 `camp.nextstep.edu.missionutils.Randoms`의 `pickNumberInRange()`를 활용하여 1~9 범위의 정수 난수 3 개 생성
- 이전과 같은 난수일 경우 다를 때까지 재생성

### 사용자로부터 서로 다른 세 자리 숫자 입력 받기 및 예외 처리

- 사용자 입력은 `camp.nextstep.edu.missionutils.Console`의 `readLine()`을 활용
- 중복된 수 존재 or 세 자리 숫자가 아닐 경우 `IllegalArgumentException` 예외 발생 후 종료

### 게임 진행

#### 포수 판정 - 생성된 수와 사용자 입력을 비교

- index 같음 and 수 같음 -> 스트라이크 + 1
- index 다름 and 수 같음 -> 볼 + 1
- 모든 index 다름 and 수 다름 -> 낫싱
- 모든 index의 수 같음 -> 승리

#### 다시 시작 or 게임 종료

- 게임이 끝난 경우 사용자에게 1 or 2의 입력받음
- 1인 경우 다시 시작
- 2인 경우 게임 종료
- 잘못된 입력 받을 경우 `IllegalArgumentException` 예외 발생 후 종료
## 📝 License

This project is [MIT](https://github.com/woowacourse/java-baseball-precourse/blob/master/LICENSE) licensed.
