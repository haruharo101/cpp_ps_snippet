> WINDOWS

1. Win + R을 통해 실행창을 열어주세요.

2. %appdata%를 입력하고 엔터를 눌러주세요.

3. Code > User > snippets 에 있는 cpp.json을 이 프로젝트에 있는 cpp.json으로 교체해주세요.

4. 이제 VSCode에서 키워드를 입력하면 템플릿을 쓸 수 있습니다.


> 현재 제작한 템플릿

- hd(미완) : 헤더입니다. 자신의 핸들, 깃헙 핸들을 적을 수 있으며, bits/stdc++.h 헤더를 include 하고 기본적인 변수들을 설정합니다.
(amod : AtCoder에서 자주 사용하는 값(998244353), mod : 10**9+7.)

- tc : 테스트케이스가 주어지는 문제에서 사용할 수 있습니다. (ex. CodeForces)

- rep1 : 1중 반복문을 출력합니다.

- rep2 : 2중 반복문을 출력합니다.

- fib : 기본적인 피보나치 수열의 값을 1항부터 1 000 000항까지 구해냅니다. O(N).

- ssum : C++에서의 큰 수 덧셈을 문자열로 구해줍니다. ssum(string, string)으로 호출하면 string이 return됩니다.
(https://www.acmicpc.net/problem/15353)
