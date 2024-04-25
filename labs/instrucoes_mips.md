# Principais instruções Assembly MIPS

| Instrução | Descrição                                                                                       |
|-----------|-------------------------------------------------------------------------------------------------|
| `add`     | Adiciona dois registradores e armazena o resultado em um terceiro registrador.                 |
| `addi`    | Adiciona um valor imediato a um registrador e armazena o resultado em um terceiro registrador. |
| `addu`    | Adiciona dois registradores sem sinal e armazena o resultado em um terceiro registrador.       |
| `addiu`   | Adiciona um valor imediato sem sinal a um registrador e armazena o resultado em um registrador.|
| `sub`     | Subtrai o conteúdo de dois registradores e armazena o resultado em um terceiro registrador.    |
| `subu`    | Subtrai dois registradores sem sinal e armazena o resultado em um terceiro registrador.        |
| `mult`    | Multiplica dois registradores de 32 bits e armazena o resultado nos registradores HI e LO.     |
| `div`     | Divide dois registradores de 32 bits e armazena o quociente em LO e o resto em HI.             |
| `and`     | Realiza a operação lógica AND bit a bit entre dois registradores e armazena o resultado.       |
| `or`      | Realiza a operação lógica OR bit a bit entre dois registradores e armazena o resultado.        |
| `ori`     | Realiza a operação lógica OR bit a bit entre um registrador e um valor imediato.               |
| `xor`     | Realiza a operação lógica XOR bit a bit entre dois registradores e armazena o resultado.       |
| `nor`     | Realiza a operação lógica NOR bit a bit entre dois registradores e armazena o resultado.       |
| `sll`     | Realiza um deslocamento à esquerda lógico em um registrador.                                   |
| `srl`     | Realiza um deslocamento à direita lógico em um registrador.                                    |
| `sra`     | Realiza um deslocamento à direita aritmético em um registrador.                                |
| `slt`     | Define um registrador de destino como 1 se o primeiro operando for menor que o segundo.       |
| `slti`    | Define um registrador de destino como 1 se o primeiro operando for menor que o imediato.     |
| `beq`     | Desvia a execução do programa se dois registradores forem iguais.                              |
| `bne`     | Desvia a execução do programa se dois registradores não forem iguais.                          |
| `j`       | Salta para um endereço especificado.                                                            |
| `jal`     | Salta para um endereço especificado e armazena o endereço de retorno em `$ra`.                |
| `jr`      | Salta para o endereço contido em um registrador.                                               |
| `lw`      | Carrega uma palavra da memória para um registrador.                                            |
| `sw`      | Armazena uma palavra de um registrador na memória.                                             |ma palavra de um registrador na memória.                                             |