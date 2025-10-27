# palindrome  

**AIM**:
 Write an assembly language program in 8086 to check whether a given number is a palindrome or not
 
 **APPARATUS REQUIRED**
   personal computer with Masm software
 
****PROGRAM**
```
STACK SEGMENT
 DW 128 DUP(?)
STACK ENDS

DATA SEGMENT
    msg1 DB 13,10,'PALINDROME$'
    msg2 DB 13,10,'NOT PALINDROME$'
DATA ENDS

CODE SEGMENT
ASSUME CS:CODE, DS:DATA

START:
    MOV AX, DATA
    MOV DS, AX         
    MOV AL, 22
 MOV AH, 0          
    MOV BL, 10         
    DIV BL       

    CMP AL, AH
    JNE NOTPAL       

PAL:                   
    LEA DX, msg1        
    MOV AH, 09H
    INT 21H
    JMP EXIT

NOTPAL:                 
    LEA DX, msg2        
    MOV AH, 09H
    INT 21H

EXIT:
    MOV AH, 4CH       
    INT 21H
CODE ENDS
END START
```
**OUTPUT**
  ![WhatsApp Image 2025-10-27 at 12 30 23_bf94e0d1](https://github.com/user-attachments/assets/97a74ca6-fb4d-4e2a-a3d4-31cd283f4d05)
  ![WhatsApp Image 2025-10-27 at 12 30 56_cc85ef72](https://github.com/user-attachments/assets/9a4dc049-b788-4033-8f32-b8b1f5121203)
  ![WhatsApp Image 2025-10-27 at 12 31 59_87a27fb7](https://github.com/user-attachments/assets/cec33cc2-19b2-453e-aa3a-a81560f5c535)
  
**RESULT**
Thus the assembly language program in 8086 to check whether a given number is a palindrome or not shown in output
