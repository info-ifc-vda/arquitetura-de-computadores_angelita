
# Atividade Prática: Operações de load e store em Assembly MIPS

- **Exemplo 1: Usando `lw` (load word)**

Escreva um programa que carregue um valor da memória

  ```assembly
  .data
      var1: .word 100
  .text
  .globl main
  main:
      la $t0, var1      # Carrega o endereço de var1 em $t0
      lw $t1, 0($t0)    # Carrega a palavra na memória apontada por $t0 em $t1
      # $t1 agora contém o valor 100
  ```

- **Exemplo 2: Usando `sw` (store word)**

Escreva um programa que armazene um valor na memória

  ```assembly
  .data
      var2: .word 0
  .text
  .globl main
  main:
      li $t2, 200       # Carrega o imediato 200 em $t2
      la $t3, var2      # Carrega o endereço de var2 em $t3
      sw $t2, 0($t3)    # Armazena o conteúdo de $t2 na memória em var2
      # var2 na memória agora contém o valor 200
  ```
Se o objetivo é criar um exemplo onde o array já está pré-definido e manipulamos esses dados sem interação com o usuário, podemos ajustar o Exemplo 3 para demonstrar a manipulação de um array com valores pré-definidos, dobrando cada valor e então exibindo os resultados.

### Exemplo 3: Manipulação de Dados com Array 

Escreva um programa que contém um array de cinco números inteiros. O programa deve dobrar cada valor do array e exibir os valores modificados.

```assembly
.data
    array: .word 10, 20, 30, 40, 50  # Array de 5 elementos
    size: .word 5                     # Tamanho do array
    output: .asciiz "Valor dobrado: "

.text
.globl main
main:
    la $t0, array       # $t0 mantém o endereço base do array
    lw $t1, size        # $t1 é o contador do loop
    li $t2, 0           # $t2 é o índice atual do array

process_loop:
    # Verificar se o loop deve continuar
    beq $t2, $t1, end_loop

    # Carregar o valor atual do array
    lw $t3, 0($t0)      # $t3 recebe o valor na posição atual do array

    # Dobrar o valor
    sll $t3, $t3, 1     # Multiplica $t3 por 2 (shift left logical)

    # Armazenar o valor dobrado de volta no array
    sw $t3, 0($t0)      # Armazena $t3 na posição atual do array

    # Avançar para o próximo elemento do array
    addi $t0, $t0, 4    # Incrementa o endereço do array para o próximo inteiro (4 bytes)
    addi $t2, $t2, 1    # Incrementa o índice do array

    j process_loop      # Salta para o início do loop

end_loop:
    # Resetar o ponteiro e o índice para imprimir os valores
    la $t0, array       # Reset $t0 ao início do array
    li $t2, 0           # Reset $t2 ao índice inicial

print_loop:
    # Verificar se o loop deve continuar
    beq $t2, $t1, exit

    # Carregar o valor dobrado do array
    lw $t3, 0($t0)      # Carrega o valor dobrado na posição atual

    # Imprimir o valor
    li $v0, 4           # Syscall para imprimir string
    la $a0, output
    syscall

    li $v0, 1           # Syscall para imprimir inteiro
    move $a0, $t3
    syscall

    # Avançar para o próximo elemento do array
    addi $t0, $t0, 4    # Incrementa o endereço do array para o próximo inteiro
    addi $t2, $t2, 1    # Incrementa o índice do array

    j print_loop        # Salta para o início do loop de impressão

exit:
    # Sair do programa
    li $v0, 10          # Código de syscall para sair
    syscall
```


#### Parte 3: Atividade Prática
- **Descrição da Atividade:** Escreva um programa que leia vários valores de entrada, armazene-os em um array na memória e, em seguida, calcule a soma desses valores utilizando as instruções de _load_ e _store_.