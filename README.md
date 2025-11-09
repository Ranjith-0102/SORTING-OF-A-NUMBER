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

```asm
ORG 00H
LOOP1:MOV R0,#40H
MOV R6,30H
DEC R6
LOOP:MOV A,@R0
INC R0
MOV B,@R0
CJNE A,B,NEXT
NEXT:JC DOWN
MOV@R0,A
DEC R0
MOV@R0,B
INC R0
DOWN:DJNZ R6,LOOP
MOV R1,#02H
DJNZ R1,LOOP1
END



```
## OUTPUT(Ascending order)
<img width="907" height="713" alt="Screenshot 2025-11-09 150343" src="https://github.com/user-attachments/assets/7d88d9a3-a6d5-49a7-9a36-531e3f783361" />


<img width="891" height="728" alt="Screenshot 2025-11-09 150414" src="https://github.com/user-attachments/assets/2801e40f-4e5b-4c60-98aa-25fdee39ddbb" />

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

```asm
ORG 00H
LOOP1:MOV R0,#40H
MOV R6,30H
DEC R6
LOOP:MOV A,@R0
INC R0
MOV B,@R0
CJNE A,B,NEXT
NEXT:JNC DOWN
MOV@R0,A
DEC R0
MOV@R0,B
INC R0
DOWN:DJNZ R6,LOOP
MOV R1,#02H
DJNZ R1,LOOP1
END



```
## OUTPUT(Descending order)

<img width="1013" height="718" alt="Screenshot 2025-11-09 150931" src="https://github.com/user-attachments/assets/e22de446-f798-4abc-9a41-e66b0d7d3441" />

<img width="1143" height="632" alt="Screenshot 2025-11-09 151007" src="https://github.com/user-attachments/assets/edfb6789-93de-4772-86bf-ef7f792e0ba9" />

---
## RESULT:
Thus the sorting of given data was done using 8051 keil software.

