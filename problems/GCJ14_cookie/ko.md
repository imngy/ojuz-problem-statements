### 도입

*Cookie Clicker*는 Orteil이 만든 Javascript 게임으로, 이 게임에서 참가자들은 거대한 쿠키의 사진을 누릅니다. 거대한 쿠키를 누르면 쿠키들을 받습니다. 그들은 이 쿠키들을 건물을 짓는 데에 소비할 수 있습니다. 이 건물들은 참가자들이 더 많은 쿠키를 얻을 수 있게 도와줍니다. 이 문제와 같이, 게임은 매우 쿠키에 초점을 맞추고 있습니다. 이 문제는 비슷한 아이디어를 가지고 있지만, 여러분이 *Cookie Clicker*를 한 적 있다는 가정을 하지는 않습니다. 지금 가서 하지는 마세요: 돌아오기까지 많은 시간이 걸릴 지도 모릅니다.

### 문제

이 문제에서, 여러분은 처음에 0개의 쿠키를 가지고 있습니다. 여러분은 거대한 쿠키를 클릭하여 쿠키 2개/1초의 비율로 쿠키를 받습니다. 여러분이 $C$개 이상의 쿠키를 가지고 있다면, 언제라도 쿠키 농장을 구매할 수 있습니다. 여러분이 쿠키 농장을 살 때마다, $C$개의 쿠키가 들며, 이 농장은 1초당 $F$개의 쿠키를 더 줍니다.

여러분이 농장을 구매하는 데 쓰지 않은 $X$개의 쿠키를 가지고 있다면, 그 순간 여러분이 이깁니다! 여러분이 최적의 전략을 사용했을 때, 이기는 데에 얼마나 걸릴지 구하는 프로그램을 작성하세요.

### 예시

$C = 500.0, F = 4.0, X = 2000.0$이라고 가정합니다. 이 때 최적의 전략은 아래와 같습니다.

1. 여러분은 처음당 0개의 쿠키를 가지고 있지만, 1초당 2개의 쿠키를 생산할 수 있습니다.
2. 250초 후, 여러분은 $C = 500$개의 쿠키를 가지고 있어, 1초당 $F = 4$개의 쿠키를 생산하는 농장 하나를 살 수 있습니다.
3. 농장을 산 이후, 여러분은 0개의 쿠키를 가지고 있고, 1초당 총 생산량은 쿠키 6개입니다.
4. 다음 농장을 사는 데에는 500개의 쿠키가 듭니다. 약 83.3333333초 후에 구매할 수 있습니다.
5. 두 번째 농장을 산 이후, 여러분은 0개의 쿠키를 가지고 있고, 1초당 총 생산량은 쿠키 10개입니다.
6. 또다른 농장을 사는 데에는 500개의 쿠키가 듭니다. 약 50초 후에 구매할 수 있습니다.
7. 세 번째 농장을 산 이후, 여러분은 0개의 쿠키를 가지고 있고, 1초당 총 생산량은 쿠키 14개입니다.
8. 또다른 농장을 사는 데에는 500개의 쿠키가 들지만, 굳이 살 필요는 없습니다. 대신 여러분은 $X = 2000$개의 쿠키를 가지고 있을 때까지 기다리면 됩니다. 약 142.8571429초가 걸립니다.

총 시간: 250 + 83.3333333 + 50 + 142.8571429 = 526.1904762초.

참고로, 여러분은 쿠키를 연속적으로 받습니다: 따라서 게임이 시작한지 0.1초가 지나면 여러분은 0.2개의 쿠키를 받게 되고, $\pi$초가 지나면 여러분은 $2\pi$개의 쿠키를 가지고 있을 것입니다.

### 입력 형식

첫 번째 줄에 테스트 케이스의 개수 $T$가 주어집니다. 이후 $T$개의 줄이 주어집니다. 각 줄에는 3개의 실수 $C$, $F$, $X$가 공백을 사이로 두고 주어집니다. 이 수들의 의미는 위에서 기술한 바와 같습니다.

$C$, $F$, $X$에는 소수점 앞에 적어도 1개의 숫자가 있으며, 소수점 뒤에는 1개에서 5개의 숫자가 있습니다. 맨 왼쪽의 숫자가 0인 경우는 없습니다. (C, F and X will each consist of at least 1 digit followed by 1 decimal point followed by from 1 to 5 digits. There will be no leading zeroes.)

### 출력 형식

각 테스트 케이스마다 "`Case #x: y`"를 한 줄에 하나씩 출력합니다. `x`는 1부터 시작하는 테스트 케이스 번호이고, `y`는 여러분이 $X$개의 쿠키를 가지는 데 필요한 최소 시간입니다.

우리는 `y`를 소수점 아래 일곱 번째 자리($10^{-7}$)까지 출력하는 것을 권장하지만, 꼭 필요한 것은 아닙니다. `y`가 정확한 답과 충분히 가까워야 정답으로 인정됩니다. 절대/상대 오차는 최대 $10^{-6}$까지만 허용됩니다. [FAQ](https://code.google.com/codejam/faq.html#floating_point)에서 이것이 무엇을 의미하는지, 그리고 어떤 형태의 실수들만이 정답 처리되는지 읽어보세요.

### 제약 조건

$1 \le T \le 100$

#### Small dataset (8점)

* $1 \le C \le 500$
* $1 \le F \le 4$
* $1 \le X \le 2000$

#### Large dataset (11점)

* $1 \le C \le 10000$
* $1 \le F \le 100$
* $1 \le X \le 100000$

### 예제

<table class='table table-bordered table-condensed'>
 <thead>
  <tr>
   <th>입력</th>
   <th>출력</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td style="width: 50%;" class="code-font">4<br>
30.0 1.0 2.0<br>
30.0 2.0 100.0<br>
30.50000 3.14159 1999.19990<br>
500.0 4.0 2000.0</td>
   <td class="code-font">Case #1: 1.0000000<br>
Case #2: 39.1666667<br>
Case #3: 63.9680013<br>
Case #4: 526.1904762
</td>
  </tr>
 </tbody>
</table>