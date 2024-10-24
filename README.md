# -assembly
#Exercício:Escreva um programa em MIPS que leia dois números realize a soma de ambos e depois receba um outro numero que será subtraído do valor da soma

.data

num1: .asciiz "Digite o 1° numero: "
num2: .asciiz "Digite o 2° numero: "
num3: .asciiz "Digite o 3° numero: "

.text

li $v0,4 
la $a0, num1 
syscall 

li $v0,5 
syscall 

move $t0, $v0 
li $v0,4 
la $a0, num2 
syscall 

li $v0,5 ro
syscall 0
move $t1, $v0 

add $t2,$t1,$t0

li $v0,4 
la $a0, num3 
syscall 

li $v0,5 ro
syscall 
move $t3, $v0 

sub $t4, $t2,$t3
li $v0,1 
move $a0, $t4 
syscall 

li $v0, 10 
syscall
