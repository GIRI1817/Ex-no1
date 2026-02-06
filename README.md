# Arithmetic-operation-using-8086
# 8086 Assembly Language Programs for Arithmetic Operations

## AIM

To write and execute Assembly Language Programs to perform arithmetic operations for the 8086 microprocessor.

---

## APPARATUS REQUIRED

* Personal Computer with MASM Software

---

## 1. ADDITION

#### Algorithm

1. Initialize memory location in HL register.
2. Store 1st data.
3. Increment HL to enter 2nd data.
4. Move 2nd number to accumulator.
5. Decrement HL.
6. Add value in memory with accumulator.
7. Store result.
8. Stop.


## FLOW CHART
<img width="707" height="1024" alt="image" src="https://github.com/user-attachments/assets/b5a7062d-e294-47cd-9683-a40de25e82de" />


#### Program

```asm
CODE SEGMENT
ASSUME CS:CODE, DS:CODE
ORG 1000H
MOV CL,00H
MOV AX,1234H
MOV BX,1234H
ADD AX,BX
JNC L1
INC CL
L1:MOV SI,1200H
MOV [SI],AX
MOV [SI+2],CL
MOV AH,4CH
INT 21H
CODE ENDS
END
```


#### Manual Calculations

![WhatsApp Image 2026-02-06 at 11 08 03](https://github.com/user-attachments/assets/d3dbc7db-ae62-4b69-b4a0-cfcc31e9e719)


## OUTPUT IMAGE FROM MASM SOFTWARE
<img width="648" height="437" alt="add" src="https://github.com/user-attachments/assets/c8c09277-7962-47c1-82e0-b935fe0c900e" />

## 2. SUBTRACTION

#### Algorithm

1. Initialize memory and store 1st data.
2. Increment to get 2nd data.
3. Move 2nd data to accumulator.
4. Subtract memory content.
5. Store result.

## FLOWCHART

<img width="578" height="797" alt="image" src="https://github.com/user-attachments/assets/564c3c7a-33ce-4a1c-8920-beb5c24b9b47" />


#### Program
```asm
code segment
assume cs:code,ds:code
org 1000h
mov AX,1234h
mov BX,1234h
sub AX,BX
jnc down
inc CL
down:mov SI,1200h
mov [sI],AX
mov [SI+2],CL
mov ah,4ch
int 21H
code ends
end
```




#### Manual Calculations

![WhatsApp Image 2026-02-06 at 11 08 41](https://github.com/user-attachments/assets/62fa7d36-7466-4573-b7f8-0697bf87526c)



## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="647" height="439" alt="sub" src="https://github.com/user-attachments/assets/b552df8b-4bd5-4348-ac68-e96430c2faed" />

## 3. MULTIPLICATION

#### Algorithm

1. Initialize memory and store operands.
2. Move operands to registers.
3. Multiply.
4. Store result.

##FLOWCHART

<img width="569" height="906" alt="image" src="https://github.com/user-attachments/assets/88be88ff-2896-4a88-b73d-84ccffd2fcf9" />



#### Program

```asm
code segment
assume cs:code,ds:code
org 1000h
MOV DX,0000H
mov AX,1234h
mov BX,1234h
mul BX
mov si,1200h
mov [si],ax
mov [si+02h],dx
mov ah,4ch
int 21h
code ends
end
```



#### Manual Calculations

![WhatsApp Image 2026-02-06 at 11 06 45](https://github.com/user-attachments/assets/a3c6cbac-6773-44e1-bd20-53994a38918d)


## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="644" height="439" alt="mul" src="https://github.com/user-attachments/assets/6bb6c0ed-19e9-41e3-96ba-f2a31be6ded8" />

## 4. DIVISION

#### Algorithm

1. Load memory location of operands.
2. Perform division.
3. Store result.

   ## FLOWCHART
<img width="1065" height="802" alt="image" src="https://github.com/user-attachments/assets/25b4a483-0d42-494b-8639-1af3ea17191b" />


#### Program

```asm
CODE SEGMENT
ASSUME CS:CODE,DS:CODE
ORG 1000H
MOV DX,0000H
MOV AX,1234H
MOV BX,1234H
DIV BX
MOV SI,1200H
MOV [SI],AX
MOV [SI+2H],DX
MOV AH,4CH
INT 21H
CODE ENDS
END
```


#### Manual Calculations

![WhatsApp Image 2026-02-06 at 11 06 45 (1)](https://github.com/user-attachments/assets/610c4937-867e-414f-ba88-5af3d1187826)

## OUTPUT FROM MASM SOFTWARE
<img width="649" height="434" alt="div" src="https://github.com/user-attachments/assets/f5a477d5-22c6-49ad-a317-37680f6724a4" />



## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.

