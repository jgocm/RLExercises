### *Exercise 3.8:*

**Suppose y = 0.5 and the following sequence of rewards is received R 1 = 1,
R 2 = 2, R 3 = 6, R 4 = 3, and R 5 = 2, with T = 5. What are G 0 , G 1 , . . ., G 5 ? Hint:
Work backwards.**

---
Resposta:

```
G5 = 0, pois T = 5.

G4 = R5 + y*G5 = 2
G3 = R4 + y*G4 = 4
G2 = R3 + y*G3 = 8
G1 = R2 + y*G2 = 6
G0 = R1 + y*G1 = 2

```
