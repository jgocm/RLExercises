### *Exercise 2.2: Bandit example*

**Consider a k-armed bandit problem with k = 4 actions, denoted 1, 2, 3, and 4. Consider applying to this problem a bandit algorithm using "-greedy action selection, sample-average action-value estimates, and initial estimates of Q1(a) = 0, for all a. Suppose the initial sequence of actions and rewards is A1 = 1, R1 = -1, A2 = 2, R2 = 1, A3 = 2, R3 = -2, A4 = 2, R4 = 2, A5 = 3, R5 = 0. On some of these time steps the ε case may have occurred, causing an action to be selected at random. On which time steps did this definitely occur? On which time steps could this possibly have occurred?**

---
Resposta 1:

```
Conjunto de Ações e Recompensas:
A1 = 1; R1 = -1
A2 = 2; R2 = 1
A3 = 2; R3 = -2
A4 = 2; R4 = 2
A5 = 3; R5 = 0

Computando as qualidades das ações a cada iteração:
- t=0: Q(a)=0, para todos os valores de a
- t=1: atualiza o valor Q(a=1)=-1
- t=2: atualiza o valor Q(a=2)=1
- t=3: atualiza o valor Q(a=2)=(1-2)/2=-0,5
- t=4: atualiza o valor Q(a=2)=(1-2+2)/3=0,333
- t=5: mantem o valor Q(a=3)=0

Assim, podemos computar a seguinte tabela com os valores de Qt(a):
|     | Qt(a=1) | Qt(a=2) | Qt(a=3) | Qt(a=4) |
|:---:|:-------:|:-------:|:-------:|:-------:|
| t=0 |    0    |    0    |    0    |    0    | a=1 =>   Ação tomada aleatoriamente => pode ter ocorrido uma ação 'e'
| t=1 |    -1   |    0    |    0    |    0    | a=2 =>   Ação tomada aleatoriamente entre as 3 gulosas => pode ter ocorrido uma ação 'e'
| t=2 |    -1   |    1    |    0    |    0    | a=2 =>   Escolhe a ação gulosa => pode ter ocorrido uma ação 'e'
| t=3 |    -1   |   -0,5  |    0    |    0    | a=2 =>   Escolhe ação não-gulosa => com certeza ocorreu uma ação 'e'
| t=4 |    -1   |  0,333  |    0    |    0    | a=3 =>   Escolhe ação não-gulosa => com certeza ocorreu uma ação 'e'
| t=5 |    -1   |  0,333  |    0    |    0    |


```
