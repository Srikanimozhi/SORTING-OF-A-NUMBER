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

ORG 0000H 
MOV R7,#4 
LOOP1:MOV R0,#40H 
MOV R6,#04 
LOOP: MOV A,@R0 
INC R0 
MOV 50H,@R0 
CJNE A,50H,NEXT 
SJMP DOWN 
NEXT:JC DOWN 
MOV @R0,A 
DEC R0 
MOV @R0,50H 
DOWN:DJNZ R6,LOOP 
DJNZ R7,LOOP1 
END 



```
## OUTPUT(Ascending order)

<img width="1919" height="1140" alt="Screenshot 2025-10-03 090434" src="https://github.com/user-attachments/assets/7995fd24-3b6f-4fa9-a53b-d3e57b4bbb14" />

![WhatsApp Image 2025-11-06 at 23 48 29_6a3a7d2e](https://github.com/user-attachments/assets/1e13b40f-45d0-4800-b175-981aa92b14da)

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


ORG 0000H 
MOV R7,#4 
LOOP1:MOV R0,#40H 
MOV R6,#04 
LOOP: MOV A,@R0 
INC R0 
MOV 50H,@R0 
CJNE A,50H,NEXT 
SJMP DOWN 
NEXT:JNC DOWN 
MOV @R0,A 
DEC R0 
MOV @R0,50H 
DOWN:DJNZ R6,LOOP 
DJNZ R7,LOOP1 
END

```
## OUTPUT(Descending order)
<img width="1916" height="1121" alt="Screenshot 2025-10-03 085411" src="https://github.com/user-attachments/assets/f5dc3b41-afd8-4058-bea4-e94eb3437213" />

![WhatsApp Image 2025-11-06 at 23 48 29_82c272ba](https://github.com/user-attachments/assets/f843bfdd-393a-48aa-a5bd-4c757fe399a1)


---
## RESULT:
Thus the sorting of given data was done using 8051 keil software.

