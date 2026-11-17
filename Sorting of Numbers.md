# sorting-of-numbers
## Aim
To write and execute an Assembly Language Program for sorting data in Ascending and  descending order using 8051 microcontroller on Keil software.
---

## Apparatus Required
- Personal Computer  
- Keil µVision software  
---

## Algorithm(ASCENDING ORDER)
1. Initialize the register **R7** with count (number of elements).  
2. Get the first two elements into two registers.  
3. Compare the two elements:  
   - If the value in register **R0** is lower, exchange **A** and **R0** data.  
   - Otherwise, increment pointer and decrement register **R7**.  
4. Check if **R7 = 0** → if yes, move the register **R0 & A**.  
5. Increment pointer and decrement **R7**.  
6. If **R7 ≠ 0**, repeat from Step 2.  
7. Otherwise, stop the program.  
---

## Program (Ascending order)

```

ORG 0000H

MOV 30H,#02H
MOV 31H,#08H
MOV 32H,#0BH
MOV 33H,#0FH
MOV 34H,#10H
MOV 35H,#1AH

MOV R2,#05H

LOOP1:
MOV R0,#30H
MOV R3,#05H

LOOP2:
MOV A,@R0
MOV 40H,A
INC R0

MOV A,@R0
CJNE A,40H,CHECK

SJMP NEXT

CHECK:
JC NEXT

MOV 41H,A
MOV A,40H
MOV @R0,A
DEC R0
MOV A,41H
MOV @R0,A
INC R0

NEXT:
DJNZ R3,LOOP2
DJNZ R2,LOOP1

HERE: SJMP HERE

END




```
## OUTPUT(Ascending order)
<img width="1536" height="864" alt="image" src="https://github.com/user-attachments/assets/6f552d8e-1655-458d-b4f1-16e0aa66f679" />



---

## Algorithm(Descending order)
1. Initialize the register **R7** with count.  
2. Get first two elements in two registers.  
3. Compare the two elements of data:  
   - If the value of **R0** register is high, then exchange **A** and **R0** data.  
   - Else, increment pointer and decrement register **R7**.  
4. Check if **R7 = 0**, then move the contents of **R0** and **A**.  
5. Again increment pointer and decrement **R7**.  
6. Check if **R7 = 0**:  
   - If **No**, repeat the process from Step 2.  
   - If **Yes**, stop the program.  
---
## Program (Descending order)

```

ORG 0000H

MOV 50H,#02H
MOV 51H,#08H
MOV 52H,#0BH
MOV 53H,#0FH
MOV 54H,#10H
MOV 55H,#1AH

MOV R2,#05H

LOOP1:
MOV R0,#50H
MOV R3,#05H

LOOP2:
MOV A,@R0
MOV 40H,A
INC R0

MOV A,@R0
CJNE A,40H,CHECK

SJMP NEXT

CHECK:
JNC NEXT

MOV 41H,A
MOV A,40H
MOV @R0,A
DEC R0
MOV A,41H
MOV @R0,A
INC R0

NEXT:
DJNZ R3,LOOP2
DJNZ R2,LOOP1

HERE: SJMP HERE

END



```
## OUTPUT(Descending order)
<img width="1536" height="864" alt="image" src="https://github.com/user-attachments/assets/32638e2b-e2c0-447c-8574-47fae6af3bf4" />



---
## RESULT:
Thus the sorting of given data was done using 8051 keil software.

