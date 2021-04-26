
TSP : Traveling Salesperson Problem!;
Hamiltonian cycle: visit each node once cylce

shortest H.C 을 찾는문제. 

dp와 bit_mask를 이용하여 문제를 해결한다. 

dp[vi][va,vb,vc...] : start 에서 시작하여 vi에 도착하는 path중에 vertex a , b ,c,... 를 임의의 순서로 단 한번씩만 거처서 도착하는 최소 거리 로 정의 한다. 


그렇다면 dp[vi][va,vb,vc...] 의 후보를 살펴보자. 

최소 거리 문제임으로 최소거리의 부분 문제는 최소거리를 갖는다는 성질을 사용할수 있고. 최소거리의 조합으로 만들수 있는 path가 후보가 될 수 있을겄이다. 


dp[vi][va,vb,vc..] = min(  dp[va][vb,vc...] +  w[va][vi]   ,  dp[vb][va,vc...] + w[vb][vi]   ,   dp[vc][va,vb...] + w[vc][vi]   );

