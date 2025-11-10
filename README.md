# 8-Bit-Arithmetic-Operations-Using-8051

## Aim:
To perform 8-bit arithmetic operations such as addition, subtraction, multiplication, and division using the 8051 microcontroller.

## Apparatus Required:

•	Laptop with Keil uVision software

## Algorithm:

## For Addition:
1.	Load the first number from memory location 30H into register A.
2.	Load the second number from memory location 31H into register B.
3.	Add the contents of registers A and B.
4.	Store the result in memory location 40H.
5.	Store the carry (if any) in 41H.

## Program:
```
ORG 0000H
MOV A, 30H     
ADD A, 31H    
MOV 40H, A 
JNC NEXT 
MOV 41H, #01H
SJMP END_PROGRAM
NEXT: MOV 41H, #00H
END_PROGRAM: NOP
END
```

## Output:
<img width="1919" height="1140" alt="image" src="https://github.com/user-attachments/assets/21bd48e1-38fc-4fa5-bba8-b0fff7e33055" />
<img width="1919" height="1139" alt="image" src="https://github.com/user-attachments/assets/d622d80a-fe0b-4292-8f8c-cf06123d0a6a" />

   
## For Subtraction:
1.	Load the first number from memory location 30H into register A.
2.	Load the second number from memory location 31H into register B.
3.	Subtract B from A.
4.	Store the result in memory location 40H.

## Program:
```
ORG 0000H;
	MOV A, 30H;
	SUBB A,31H;
	MOV 40H,A;
	JNC NEXT;
	MOV 41H,#01H;
	SJMP END_PROGRAM;
	NEXT:MOV 41H,#00H;
	END_PROGRAM:NOP;
	END;
```

## Output:
<img width="1910" height="912" alt="Screenshot 2025-11-10 121812" src="https://github.com/user-attachments/assets/78571ece-c323-454d-97c5-f02a72d12428" />
<img width="1915" height="909" alt="Screenshot 2025-11-10 121832" src="https://github.com/user-attachments/assets/6b61a605-0629-4cdc-8c80-9bcf9fd8f641" />
## For Multiplication:
1.	Load the first number from memory location 30H into register A.
2.	Load the second number from memory location 31H into register B.
3.	Multiply A and B.
4.	Store the lower byte of the result in memory location 40H.
5.	Store the higher byte of the result in memory location 41H.

## Program:
```
ORG 0000H
MOV A, 30H 
MOV B, 31H
MUL AB
MOV 40H, A 
MOV 41H, B
END
```

## Output:
<img width="1918" height="1137" alt="image" src="https://github.com/user-attachments/assets/399c4ab6-c58c-41ca-a293-d010b2e46d9e" />
<img width="1919" height="1137" alt="image" src="https://github.com/user-attachments/assets/79e572cb-7e8f-4180-84af-7fd950c09ac2" />



## For Division:
1.	Load the dividend from memory location 30H into register A.
2.	Load the divisor from memory location 31H into register B.
3.	Divide A by B.
4.	Store the quotient in memory location 40H.
5.	Store the remainder in memory location 41H.


## Program:
```
ORG 0000H;
	MOV A,30H;
	MOV B,31H;
	DIV AB;
	MOV 40H,A;
	MOV 41H,B;
	END;
```



## Output:
<img width="1920" height="1080" alt="MPMCEXP5DIVIN" src="https://github.com/user-attachments/assets/3991dab2-fe54-45e2-8090-4a0b94fba6a4" />
<img width="1920" height="1080" alt="MPMCEXP5DIVOP" src="https://github.com/user-attachments/assets/0d8501e9-4b0b-472c-b6fb-897818d1eef1" />




## Result:

## Result:
The 8-bit arithmetic operations using the 8051 microcontroller have been successfully executed and verified using Keil software.

