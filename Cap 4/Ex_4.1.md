### *Exercise 4.1:*

**In Example 4.1, if π is the equiprobable random policy, what is qπ(11, down)? What is qπ(7, down)?**

---
Resposta:

```
Assumindo γ=0,9

A primeira ação move para o estado terminal então:
qπ(11, down) = Eπ[Rt+1 + γvπ(St+1) | St = s, At = a] = -1 + 0,9*0 = -1

Na segunda pergunta, a ação move para o estado 11, com vπ(11) = -14, logo:
qπ(7, down) = Eπ[Rt+1 + γvπ(St+1) | St = s, At = a] = -1 + 0,9*(-14) = -13,6

```
