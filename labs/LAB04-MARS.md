### Atividade Prática: Operações de Soma em Assembly MIPS

#### Objetivo:
Desenvolver habilidades em programação em assembly MIPS focando em diferentes formas de realizar a operação de soma.

#### Exercício 1: Soma de Constantes
Escreva um programa que soma dois números constantes e imprima o resultado.

```assembly
.data
.text
.globl main
main:
    li $t0, 15       # Carrega o número 15 no registrador $t0
    li $t1, 25       # Carrega o número 25 no registrador $t1
    add $t2, $t0, $t1  # Soma $t0 e $t1, resultado em $t2

    # Preparando para imprimir o resultado
    li $v0, 1        # Código da syscall para imprimir um inteiro
    move $a0, $t2    # Move o resultado para $a0, o registrador de argumento
    syscall          # Executa a syscall

    # Sair do programa
    li $v0, 10       # Código da syscall para sair do programa
    syscall
```

#### Exercício 2: Soma de Valores Armazenados na Memória
Modifique o programa para somar valores armazenados em locais de memória especificados.

```assembly
.data
    num1: .word 30
    num2: .word 40
.text
.globl main
main:
    lw $t0, num1     # Carrega o valor de num1 em $t0
    lw $t1, num2     # Carrega o valor de num2 em $t1
    add $t2, $t0, $t1  # Soma $t0 e $t1, resultado em $t2

    # Preparando para imprimir o resultado
    li $v0, 1
    move $a0, $t2
    syscall

    # Sair do programa
    li $v0, 10
    syscall
```

#### Exercício 3: Soma de Entradas do Usuário
Escreva um programa que solicite ao usuário dois números, some-os e imprima o resultado.

```assembly
.data
    prompt1: .asciiz "Digite o primeiro número: "
    prompt2: .asciiz "Digite o segundo número: "
.text
.globl main
main:
    # Solicitar o primeiro número
    li $v0, 4
    la $a0, prompt1
    syscall
    li $v0, 5       # Syscall para ler um inteiro
    syscall
    move $t0, $v0   # Armazena o valor lido em $t0

    # Solicitar o segundo número
    li $v0, 4
    la $a0, prompt2
    syscall
    li $v0, 5
    syscall
    move $t1, $v0   # Armazena o valor lido em $t1

    # Soma os números
    add $t2, $t0, $t1

    # Imprimir o resultado
    li $v0, 1
    move $a0, $t2
    syscall

    # Sair do programa
    li $v0, 10
    syscall
```

### Desafio:
Implemente a seguinte equação:

$y = (a + b) * (c - d) / e + f^2$

