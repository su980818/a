# 15681

https://www.acmicpc.net/problem/15681

각각의 vertex에서 부모를 제외하면 모두 자식이 된다.
root부터 시작하여 함수를 구현하면 부모정보를 자식에게 줄수있고 이를통해 서브트리의 vertex수를 모두 알아 낼수 있다.
dp를 이용하여 sub tree 의 vertex를 저장해놓으면 중복해서 구하는걸 피할수 있다. 

(* grape 구성시 arc를 arc의 맨 뒤쪽에다 달아서 시간초과 발생 -> 앞에다가 달기)
