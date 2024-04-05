### Introdução ao MARS

O MARS (MIPS Assembler and Runtime Simulator) é uma ferramenta de simulação de assembly MIPS que permite aos estudantes e desenvolvedores escrever, testar e depurar programas MIPS sem a necessidade de hardware MIPS real. Ele fornece um ambiente interativo e educacional para explorar os conceitos fundamentais da arquitetura MIPS, como registradores, memória, instruções e fluxo de controle.

### Prática 01: Introdução ao MARS

Nesta prática, você será introduzido ao ambiente de simulação MARS e aprenderá a escrever, compilar e executar um simples programa em assembly MIPS.

#### Passo 1: Instalação e Abertura do MARS

1. Faça o download do MARS a partir do site oficial: [MARS MIPS Simulator](http://courses.missouristate.edu/kenvollmar/mars/).
2. Descompacte o arquivo baixado em um diretório de sua escolha.
3. Execute o arquivo `Mars4_5.jar` para abrir o MARS.

#### Passo 2: Escrevendo um Programa em Assembly MIPS

1. No MARS, selecione `File` > `New` para abrir um novo arquivo.
2. Escreva o seguinte código em assembly MIPS:

```assembly
.data
mensagem: .asciiz "Olá, Mundo!\n"

.text
.globl main
main:
    li $v0, 4       # Carrega o código da syscall para imprimir string
    la $a0, mensagem    # Carrega o endereço da string para imprimir
    syscall         # Chama a syscall para imprimir a string
    li $v0, 10      # Carrega o código da syscall para sair do programa
    syscall         # Chama a syscall para sair do programa
```


#### Passo 3: Compilando e Executando o Programa

1. Selecione `Run` > `Assemble` para compilar o programa.
2. Se não houver erros, selecione `Run` > `Go` para executar o programa.
3. Você deve ver a mensagem "Olá, Mundo!" impressa na console de saída.

### Passo 4: Programa para Imprimir um Valor Inteiro

Neste passo, vamos criar um programa em assembly MIPS que imprime um valor inteiro na tela. Para isso, utilizaremos a syscall `1` (código `$v0`) para imprimir um inteiro e a syscall `10` para finalizar o programa.

#### Passo a Passo:

1. **Definir o valor a ser impresso:**
   - Usaremos a diretiva `.data` para armazenar o valor em uma variável.

2. **Carregar o valor e chamar a syscall para impressão:**
   - Utilizaremos a syscall `1` para imprimir o valor inteiro.

3. **Finalizar o programa:**
   - Usaremos a syscall `10` para sair do programa.

#### Programa em Assembly MIPS:

```assembly
.data
    numero: .word 42    # Define o número a ser impresso como 42

.text
    li $v0, 1            # Código da syscall para imprimir um inteiro
    lw $a0, numero       # Carrega o número para ser impresso
    syscall

    # Finaliza o programa
    li $v0, 10           # Código da syscall para sair do programa
    syscall
```

#### Explicações:

- Na seção `.data`, definimos a variável `numero` com o valor inteiro que queremos imprimir (nesse caso, 42).
- Em seguida, na seção `.text`, carregamos o código da syscall `1` no registrador `$v0`, indicando que queremos imprimir um inteiro.
- Usamos a instrução `lw` para carregar o valor da variável `numero` para o registrador `$a0`, que é o registrador de argumento para a syscall.
- Chamamos a syscall com a instrução `syscall`, que imprimirá o valor inteiro na tela.
- Finalmente, utilizamos a syscall `10` para encerrar o programa.

### Passo 5: Programa para Somar Dois Inteiros

Neste passo, vamos criar um programa em assembly MIPS que soma dois valores inteiros e imprime o resultado na tela. Para isso, utilizaremos a syscall `1` para imprimir o resultado e a syscall `10` para finalizar o programa.

#### Passo a Passo:

1. **Definir os valores a serem somados:**
   - Usaremos a diretiva `.data` para armazenar os valores em variáveis.

2. **Realizar a soma e armazenar o resultado:**
   - Carregaremos os valores das variáveis e utilizaremos a instrução `add` para realizar a soma.
   - Armazenaremos o resultado em uma nova variável.

3. **Imprimir o resultado na tela:**
   - Utilizaremos a syscall `1` para imprimir o resultado.

4. **Finalizar o programa:**
   - Utilizaremos a syscall `10` para sair do programa.

#### Programa em Assembly MIPS:

```assembly
.data
    valor1: .word 5       # Define o valor 1 como 5
    valor2: .word 7       # Define o valor 2 como 7
    resultado: .word 0    # Define o resultado inicial como 0

.text
    lw $t0, valor1       # Carrega o valor 1 para o registrador $t0
    lw $t1, valor2       # Carrega o valor 2 para o registrador $t1
    add $t2, $t0, $t1    # Soma os valores dos registradores $t0 e $t1 e armazena em $t2

    # Imprime o resultado
    li $v0, 1            # Código da syscall para imprimir um inteiro
    move $a0, $t2        # Move o resultado para o argumento da syscall
    syscall

    # Finaliza o programa
    li $v0, 10           # Código da syscall para sair do programa
    syscall
```

#### Explicações:

- Na seção `.data`, definimos as variáveis `valor1` e `valor2` com os valores inteiros a serem somados (5 e 7, respectivamente), e a variável `resultado` para armazenar o resultado da soma.
- Em seguida, na seção `.text`, carregamos os valores das variáveis `valor1` e `valor2` para os registradores `$t0` e `$t1`, respectivamente.
- Utilizamos a instrução `add` para somar os valores dos registradores `$t0` e `$t1`, e armazenamos o resultado no registrador `$t2`.
- Para imprimir o resultado, carregamos o código da syscall `1` no registrador `$v0` e movemos o valor de `$t2` para o registrador `$a0`, que é o registrador de argumento para a syscall de impressão.
- Finalmente, utilizamos a syscall `10` para encerrar o programa.