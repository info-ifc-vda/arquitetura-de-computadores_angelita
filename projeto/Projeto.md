## Projeto 
### Projeto 01
Arquivos com a descrição do projeto
- [Descrição do projeto 1](projeto/Trabalho%201%20-%20CCC0714%20Arquitetura%20e%20Organização%20-%202024-1.pdf)
- [Arquitetura do Lobo-Guará](projeto/Trabalho%201%20-%20Arquitetura.pdf)

- **Data de entrega: 15/05/2024**

Para facilitar o desenvolvimento do seu projeto, realize as seguintes subtarefas

#### Subtarefa 1: Desenvolvimento do Diagrama do Caminho de Dados do Processador "Lobo-Guará"

**Objetivo:** Projetar o diagrama de caixas do caminho de dados (_datapath)_ da arquitetura "Lobo-Guará", considerando os componentes essenciais para a execução das instruções e o fluxo de dados entre eles.

**Instruções:**

1. **Identificação dos Componentes Principais:**
- [ ] Liste os componentes principais que compõem o caminho de dados do processador, como o Registrador de Instruções (IR), a Unidade de Controle (UC), a Unidade Lógico-Aritmética (ULA), os registradores de uso geral, e a memória principal. 
   
2. **Definição do Fluxo de Dados:**
- [ ] Defina como as instruções serão buscadas, decodificadas e executadas dentro do processador.
- [ ] Determine como os dados serão transferidos entre os registradores, a ULA e a memória, incluindo o papel do barramento de dados e de controle.

3. **Desenho do Diagrama de Caixas:**
- [ ] Crie um diagrama de caixas representando o caminho de dados do processador "Lobo-Guará".
- [ ] Determine a disposição dos componentes e as conexões entre eles, indicando claramente o fluxo de dados e os sinais de controle.

4. **Associação dos Sinais de Controle:**
- [ ] No diagrama, indique os sinais de controle que a unidade de controle emite para cada componente do caminho de dados.
- [ ] Determine como esses sinais determinam as operações realizadas durante o ciclo de instrução, e como eles influenciam a seleção de caminhos de dados e a execução de operações na ULA.

5. **Consideração das Especificidades da Arquitetura:**
   - Leve em conta as características específicas da arquitetura "Lobo-Guará", como o conjunto de instruções suportadas e o design específico de 8 bits.
   - Assegure que o diagrama reflita estas especificidades, adaptando o design para suportar as operações de branch, jump, load, store, e operações aritméticas e lógicas.


#### Subtarefa 2: Design e Implementação da Unidade Lógico-Aritmética (ULA)

**Objetivo**: Projetar e implementar a Unidade Lógico-Aritmética (ULA) para a arquitetura "Lobo-Guará", que suportará todas as operações aritméticas e lógicas necessárias.

**Instruções:**
1. Identificação das Operações Suportadas:
- [ ] Identifique todas as operações que a ULA deve suportar, conforme definido pelo conjunto de instruções da arquitetura "Lobo-Guará", incluindo adição, subtração, operações lógicas como AND, OR, NOT, além de shifts à esquerda e à direita.
2. Projeto do Esquema Inicial da ULA:
- [ ] Desenhe um esquema inicial da ULA, detalhando como ela processará as operações aritméticas e lógicas. 
- [ ] Determine os sinais de controle necessários para cada operação e como eles serão gerados pela Unidade de Controle.
3. Implementação no Logisim Evolution:
- [ ] Implemente o esquema da ULA no Logisim Evolution, garantindo que a ULA seja capaz de realizar todas as operações especificadas com precisão.
4. Testes de Funcionalidade:
- [ ] Realize testes para verificar cada operação suportada pela ULA, garantindo que os resultados sejam precisos e consistentes.
 5. Otimização e Ajustes:
    - Faça os ajustes necessários para otimizar o desempenho da ULA dentro do contexto da arquitetura "Lobo-Guará", incluindo a eficiência e a velocidade das operações.
  
#### Subtarefa 3: Integração Completa e Testes da Arquitetura "Lobo-Guará"

**Objetivo:** Integrar todos os componentes implementados anteriormente em uma única arquitetura funcional e realizar testes para garantir que todas as instruções são executadas corretamente.

**Instruções:**

1. **Integração dos Componentes:**
   - [ ] Combine a ULA, os registradores, a unidade de controle e outros componentes necessários em um único projeto no Logisim Evolution.
   - [ ] Certifique-se de que todos os componentes estão corretamente interconectados, formando o caminho de dados completo da arquitetura "Lobo-Guará".

2. **Testes Completos do Sistema:**
   - [ ] Realize uma série de testes abrangentes para verificar a funcionalidade completa do sistema. Inclua testes para cada instrução individual e combinações de instruções para garantir que a arquitetura opera conforme esperado.
   - [ ] Verifique especialmente a correta execução de instruções de branch, jump, load, store, além de operações aritméticas e lógicas.

3. **Otimização e Ajustes Finais:**
   - [ ] Após os testes, faça os ajustes finais necessários para otimizar o desempenho e a eficiência da arquitetura.
   - [ ] Ajuste a unidade de controle e os caminhos de dados para melhorar a precisão e a velocidade das operações.

4. **Preparação para Apresentação Oral:**
   - [ ] Prepare um diagrama completo da arquitetura integrada, destacando todas as partes do caminho de dados e a funcionalidade da unidade de controle.
   - [ ] Elabore uma explicação clara sobre como a arquitetura processa diferentes tipos de instruções e como os componentes interagem durante o ciclo de instrução.

5. **Demonstração Prática:**
   - Prepare uma demonstração prática do projeto no Logisim Evolution para mostrar durante a apresentação oral.
   - Planeje demonstrar o funcionamento da arquitetura com exemplos práticos de execução de instruções.

#### Subtarefa 4: Testes e Ajustes Finais da Arquitetura "Lobo-Guará"

**Objetivo:** Realizar uma série de testes detalhados para verificar a funcionalidade completa da arquitetura "Lobo-Guará" e fazer os ajustes finais necessários para garantir que a arquitetura funcione de maneira eficiente e correta.

**Instruções:**

1. **Planejamento de Testes:**
   - [ ] Desenvolva um plano de testes que cubra todas as funcionalidades da arquitetura, incluindo cada instrução suportada e suas possíveis combinações.
   - [ ] Inclua testes para verificar o correto funcionamento da unidade de controle, da ULA, dos registradores, e de outras partes do caminho de dados.

2. **Execução dos Testes:**
   - [ ] Execute os testes conforme o plano desenvolvido, utilizando o projeto implementado no Logisim Evolution.
   - [ ] Registre os resultados de cada teste, identificando quaisquer comportamentos inesperados ou falhas na execução das instruções.

3. **Análise dos Resultados:**
   - [ ] Analise os resultados dos testes para identificar áreas que necessitam de ajustes ou melhorias.
   - [ ] Determine se há necessidade de revisão nos sinais de controle, na lógica da unidade de controle, ou na implementação das operações da ULA.

4. **Ajustes e Otimização:**
   - [ ] Faça os ajustes necessários baseados na análise dos resultados dos testes.
   - [ ] Otimização do desempenho da arquitetura, ajustando configurações para aumentar a eficiência e reduzir possíveis gargalos.

5. **Preparação para Demonstração Final:**
   - [ ] Prepare a arquitetura completa para uma demonstração final.
   - [ ] Elabore uma apresentação que inclua exemplos práticos de como a arquitetura executa as instruções após os ajustes, demonstrando a robustez e a eficácia das soluções implementadas.

#### Tarefa de Ponto Extra: Implementação do Pipeline na Arquitetura "Lobo-Guará"

**Objetivo:** Implementar e testar uma versão pipelined da arquitetura "Lobo-Guará" para melhorar o desempenho do processador através do aumento do throughput de instruções.

**Instruções:**

1. **Estudo do Pipeline:**
   - [ ] Estude os princípios básicos de pipeline em processadores, incluindo os estágios típicos como busca de instrução (IF), decodificação de instrução (ID), execução (EX), acesso à memória (MEM) e escrita no registrador (WB).
   - [ ] Identifique como estas etapas se aplicam à arquitetura "Lobo-Guará" e planeje como dividir as operações da arquitetura atual em estágios pipelined.

2. **Projeto do Pipeline:**
   - [ ] Desenhe um esquema detalhado que modifique a arquitetura "Lobo-Guará" para incorporar o pipeline.
   - [ ] Defina os mecanismos necessários para lidar com hazards de dados e controle, como forwarding e stallings, para manter a integridade das operações.

3. **Implementação no Logisim Evolution:**
   - [ ] Implemente o design pipelined no Logisim Evolution, incluindo a adição de registradores de pipeline entre os estágios para armazenar o estado intermédio das instruções.
   - [ ] Garanta que todos os sinais de controle e caminhos de dados estejam corretamente configurados para suportar a execução em pipeline.

4. **Testes de Funcionalidade:**
   - [ ] Teste o pipeline implementado com várias instruções e sequências de instruções para verificar se o pipeline está funcionando corretamente.
   - [ ] Preste atenção especial aos hazards de dados e controle, e verifique se as soluções implementadas (como forwarding e stalls) estão funcionando como esperado.

5. **Análise de Desempenho: (opcional)**
   - [ ] Compare o desempenho da arquitetura pipelined com a versão não-pipelined, medindo o throughput e o número de ciclos por instrução (CPI).
   - [ ] Analise e documente os benefícios de desempenho obtidos com a implementação do pipeline.

6. **Demonstração e Discussão:**
   - [ ] Prepare uma demonstração do projeto pipelined, mostrando como o pipeline melhora o desempenho da arquitetura.
   - [ ] Prepare-se para discutir o design, os desafios enfrentados durante a implementação, e as soluções adotadas para superar esses desafios.

### Projeto2
- [Descrição do projeto 2](projeto/Trabalho%202%20-%20CCC0714%20Arquitetura%20e%20Organização%20-%202024-1.pdf)
- [Arquitetura do Guará em Matilha](projeto/Trabalho%202%20-%20Guara%20em%20matilha1.pdf)
- [Arquitetura do Guará Focinho Longo](projeto/Trabalho%202%20-%20Guara%20Focinho%20Longo.pdf)
- [Diagramas](projeto/Trabalho%202%20-%20Diagramas.pdf)