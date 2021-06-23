### *Exercise 4.6:*

**Suppose you are restricted to considering only policies that are ε-soft, meaning that the probability of selecting each action in each state, s, is at least ε/|A(s)|.
Describe qualitatively the changes that would be required in each of the steps 3, 2, and 1, in that order, of the policy iteration algorithm for v⇤ on page 80.**

---
Resposta:

```
No passo 3, a atualização da política seria dada pela definição do ε-soft:

π(a|s) = 1 - ε + ε/|A(s)|, se a=A*=ação gulosa, caso contrário: π(a|s) = ε/|A(s)|

No passo 2 há necessidade de modificar o algoritmo, mas agora sabe-se que a política π(a|s) é dada pela definição acima.

No passo 1, a inicialização aleatória de π(a|s) deve obedecer a definição do ε-soft.

```
