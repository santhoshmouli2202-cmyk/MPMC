# Square-Cube-of-a-number-using-8051
# 8051 Square  Program

## AIM
To write and execute an Assembly language program for finding the square of a given data using 8051 microcontroller in Keil software.

## APPARATUS REQUIRED
- Personal computer
- Keil μVision IDE

## ALGORITHM
1. Enter the Assembly language program.
2. Provide the input value to Port 0 (P0).
3. Execute the program.
4. The output square value is stored in Port 2 (P2).

## PROGRAM
```

ORG 0000H

MOV A,#10H
MOV B,A
MUL AB

MOV 50H,A
MOV 51H,B

HERE: SJMP HERE

END



```

## OUTPUT
<img width="1920" height="1080" alt="{DF24FE08-4758-4FA9-8162-D81E7CCFB62E}" src="https://github.com/user-attachments/assets/6add9139-c256-4f5e-bb10-d8c4e945c686" />

## RESULT
Thus, the square of the given data is calculated using 8051 Keil.

# 8051 Cube  Program

## AIM
To write and execute an Assembly language program for finding the cube of a given data using 8051 microcontroller in Keil software.

## APPARATUS REQUIRED
- Personal computer
- Keil μVision IDE

## ALGORITHM
1. Enter the Assembly language program.
2. Provide the input value.
3. Execute the program.
4. The output cube value is stored in a memory location.

## PROGRAM
```

ORG 0000H

MOV A,#10H
MOV B,A
MUL AB

MOV R0,A
MOV A,B
MOV B,#10H
MUL AB

MOV 50H,R0
MOV 51H,A
MOV 52H,B

HERE: SJMP HERE

END



```


## OUTPUT
<img width="1536" height="864" alt="image" src="https://github.com/user-attachments/assets/eeaaabb9-0448-4c44-8bc7-074588cc9abe" />

## RESULT
Thus, the cube of the given data is calculated using 8051 Keil.


