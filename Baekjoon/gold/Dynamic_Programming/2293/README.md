<br>

# 🛠️ [2293 동전 1](http://www.acmicpc.net/problem/2293) <img height="27px" width="27px" src="https://static.solved.ac/tier_small/12.svg"/>
<br>

## 📖 문제
>n가지 종류의 동전이 있다. 각각의 동전이 나타내는 가치는 다르다. 이 동전을 적당히 사용해서, 그 가치의 합이 k원이 되도록 하고 싶다. 그 경우의 수를 구하시오. 각각의 동전은 몇 개라도 사용할 수 있다.
>
>사용한 동전의 구성이 같은데, 순서만 다른 것은 같은 경우이다.

<br><br>

## ⌨️ 입력
>첫째 줄에 n, k가 주어진다. (1 ≤ n ≤ 100, 1 ≤ k ≤ 10,000) 다음 n개의 줄에는 각각의 동전의 가치가 주어진다. 동전의 가치는 100,000보다 작거나 같은 자연수이다.

<br>

## 💻 출력
>첫째 줄에 경우의 수를 출력한다. 경우의 수는 231보다 작다.

<br><br>

<details>
  
  <summary> 
  
  ## 🎈 참고
  </summary>
  <br>
  
## 📄 로직
>각 코인의 가치를 N<sub>i</sub>, K원을 만들 수 있는 경우의 수를 dp[K]라고 할 때,
>
>- 0원을 만들 수 있는 경우의 수 : 1가지<br>
>- K원을 만들 수 있는 경우의 수 : K - N<sub>i</sub>원을 만들 수 있는 경우의 수들의 합<br>
>-> dp[K] += dp[K - N<sub>i</sub>]
>
>j = N<sub>i</sub>원부터 탐색을 하며 dp[j] += dp[j - N<sub>i</sub>]
>
>모든 동전에 대해 해당 연산 반복

</details>

<br><br>
