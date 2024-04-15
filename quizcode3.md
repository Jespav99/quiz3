'''
section .text
	global _start
_start:
mov eax,[x]
mov ebx,eax
loop:
dec ebx
imul eax,ebx
cmp ebx,1
jg loop

mov [result],eax
mov eax,1
int 0x80


section .data
x dd 7
segment .bss
result resb 1
'''
