# 2231

https://www.acmicpc.net/problem/2213

![제목 없음](https://user-images.githubusercontent.com/78835559/108795803-7fa07d80-75ca-11eb-9708-0c8b38d7ab85.png)

아무 독립 집합이나 구한다면 dfs를 통해 부모vertex가 독립집함에 포함되는지 아닌지를 알기 때문에 이를 반복한다면 독립집합을 구할수 있을껏이다.

최대 독립집함은 부모가 독립집합에 포함이 되지 않는다고 (dfs를 통해 자식 vertex에 확장을 했을 때에는) 자식을 독립집합에 포함해야 하는지 안하는지는 

최대 독립집함을 알기 전까지는 알수 없고 이는 최대 독립집함을 알기 위해서는 모든 독립집함을 알아 봐야 하기때문에 이 방법은 불가능


![화면 캡처 2021-02-23 124457](https://user-images.githubusercontent.com/78835559/108799914-f93d6900-75d4-11eb-86c7-767793e05817.png)

그렇다면 위의 top down 이 아닌 bottum up을 통해 어떤 root-index를 갖는 subtree의 독립집합의 최대값을 알고 있다면 optimal problem을 적용할수 있을것이다. 

dfs를 이용해 확장을 한다면 중요한것은 어느 vertex를 포함하는지 모두 알아야하는게 아니라 지금 확장하는 vertex가 독립집합에 포함되는지 안하는지만을
알면 되기 때문에 

dp[index][0] 은 index를 포함하지 않는 독립집합의 크기 

dp[index][1] 은 index를 포함하는 독립집합의 크기로 로 정의 하여 풀어보자. 
