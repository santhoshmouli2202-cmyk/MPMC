# FACTORIAL OF A NUMBER USING 8051 (Keil)

## AIM
To write and execute an Assembly language program to perform the factorial of a number using 8051 Keil.
---
## APPARATUS REQUIRED
- Personal computer with Keil software

---
## ALGORITHM
1. **Start**
2. **Input**: Read the number `n`.
3. **Initialize**:
   - Set factorial to `1`.
   - Set `i` to `1`.
4. **Loop**: While `i` is less than or equal to `n`:
   - Multiply factorial by `i`.
   - Increment `i` by `1`.
5. **Output**: Store or print the value of factorial.
6. **End**

---

## FLOWCHART
<img width="506" height="525" alt="image" src="https://github.com/user-attachments/assets/f3b47187-6f0f-490c-8704-f2973cb2b276" />


---

## PROGRAM
```

ORG 0000H

MOV A,#01H
MOV R0,#04H

NEXT:
MOV B,R0
MUL AB
DJNZ R0,NEXT

MOV 50H,A

HERE: SJMP HERE

END


```
## OUTPUT

<img width="1920" height="1080" alt="{D0212B36-4A23-4CDB-BBE3-B5DD2B536D5B}" src="https://github.com/user-attachments/assets/4589bf1e-77a1-4de4-8b48-560540b28a7c" />



---
## MANUAL CALCULATIONS

4!=4 * 3 * 2 * 1 

4! =24


## RESULT

Thus, the factorial of a number was calculated and executed successfully using 8051 Keil.

---


