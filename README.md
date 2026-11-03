# FACTORIAL-OF-A-NUMBER
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
<img width="506" height="525" alt="image" src="https://github.com/user-attachments/assets/5148f446-4b1c-4136-a0fd-66b9f015a311" />


## PROGRAM
```asm
ORG 0000H
MOV DPTR,#4500H
MOVX A,@DPTR
MOV R0,A
INC DPTR
ACALL FACTORIAL
MOVX @DPTR,A
SJMP THIN
FACTORIAL:DEC R0
CJNE R0,#01H,PRODUCT
SJMP THICK
PRODUCT:MOV B,R0
MUL AB
ACALL FACTORIAL
THICK: RET
THIN:RET
END

```
OUTPUT
<img width="1600" height="792" alt="image" src="https://github.com/user-attachments/assets/edc8a18e-2a45-4480-8d9f-78930cf6bd74" />

(Keil output screenshot can be inserted here)

---
## MANUAL CALCULATIONS
<img width="751" height="709" alt="image" src="https://github.com/user-attachments/assets/218b94d5-07c2-4ea6-84f1-fe9de6c079a3" />

---

RESULT

Thus, the factorial of a number was calculated and executed successfully using 8051 Keil.

---


