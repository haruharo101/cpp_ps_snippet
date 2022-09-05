# Snippet For PS (C++ & VSCode)

### OS별 설치법

> WINDOWS
1. ```Win + R```을 통해 실행창을 열어주세요.

2. ```%appdata%```를 입력하고 ```엔터```를 눌러주세요.

3. ```Code > User > snippets```에 있는 ```cpp.json```을 이 프로젝트에 있는 ```cpp.json```으로 교체해주세요.

4. 이제 ```VSCode```에서 키워드를 입력하면 템플릿을 쓸 수 있습니다.

### 스니펫 목록

#### 헤더

- ```hd```(미완) : 헤더입니다. 자신의 핸들, 깃헙 핸들을 적을 수 있으며, ```bits/stdc++.h``` 헤더를 ```include``` 하고 기본적인 변수들을 설정합니다.
(```amod``` : ```AtCoder```에서 자주 사용하는 값(```998244353```), ```mod : 10**9+7```)

```debug```를 이용하여 로컬에서는 출력되지만 백준 채점 환경에서는 출력이 안되게 할 수 있습니다. (```debug << "hello world!";```) 

(Thanks to [@junah201](https://www.github.com/junha201))

#### 함수

- ```fib``` : 기본적인 피보나치 수열의 값을 ```1```항부터 ```1 000 000```항까지 구해냅니다. ```O(N)```.

- ```ssum``` : ```C++```에서의 큰 수 덧셈을 문자열로 구해줍니다. ```ssum(string, string)```으로 호출하면 ```string```이 ```return```됩니다.
(https://www.acmicpc.net/problem/15353)

> CODE
```
int main() {
    string A, B;
    cin >> A >> B;
    cout << ssum(A, B);
}
```
> INPUT
```
32647624863284683726783647836247682364783246 2364783268463284674678326478236486237864832687
```
> OUTPUT
```
2397430893326569358405110126072733920229615933
```

- ```mers_p``` : ```2**n-1```꼴의 정수가 소수인지 판별합니다.  ``` mers_p(int)```로 호출하면 소수인 경우 ```true(1)```, 아닌 경우 ```false(0)```이 ```return```됩니다.
시간복잡도는 ```O(sqrt(int))```입니다. 코드는 [ncode님의 블로그](https://blog.naver.com/xtelite/50087283849)를 참고했습니다.

- ```geom``` : 다음 문단을 참조해 주세요.

##### geom 

- ```Point, Point_d``` : 각각 정수형 좌표와 실수```(double)```형 좌표를 저장하는 구조체입니다.

- ```pipo(pair<int, int>), pipo_d(pair<double, double>)``` : 차례대로 ```pair```형 좌표를 ```Point, Point_d``` 구조체로 변환해서 ```return``` 합니다.

- ```dist(Point A, Point B), dist_d(Point_d A, Point_d B)``` : 차례대로 정수, 실수형 좌표를 저장한 구조체 2개를 받아 두 점간의 유클리드 거리를 ```return``` 합니다. 이때, 두 함수 모두 ```double```을 ```return``` 합니다.

###### 예시

> CODE
```
int main() {
    pair<int, int> X = {0, 0};
    pair<int, int> Y = {3, 5};
    pair<double, double> Xd = {1.0, 1.0};
    pair<double, double> Yd = {4.0, 7.0};
    cout << dist(pipo(X), pipo(Y)) << '\n';
    cout << dist_d(pipo_d(Xd), pipo_d(Yd)) << '\n';
}
```
> OUTPUT
```
5.83095
6.7082
```

#### 메인

- ```tc``` : 테스트케이스가 주어지는 문제에서 사용할 수 있습니다. ```(ex. CodeForces)```

- ```rep1``` : 1중 반복문을 출력합니다.

- ```rep2``` : 2중 반복문을 출력합니다.
