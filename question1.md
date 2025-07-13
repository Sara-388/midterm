;var1 = 10
;var2 = 3
;var3 = 6
;result = 4

section .text
    global _start

_start:  
    mov eax, [var1]
    add eax, 2         
    
    mov ebx, [var3]
    sub ebx, [var2]     

    cdq                 
    idiv ebx           

    mov [result], eax   

    mov eax, 1   
    int 0x80
