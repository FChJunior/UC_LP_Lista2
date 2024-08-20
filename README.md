# LISTA DE EXERCÍCIOS Nº 2

**Unidade Operacional:** CFP – AUA  
**Curso:** Técnico Programador de Jogos Digitais  
**Modalidade:** Habilitação Técnica  
**Turma:** 2º ano  
**Módulo:** Integrador Introdutório  
**Unidade Curricular:** Lógica de Programação  
**Conteúdo:** Condicionais

**Observações:**
- Crie cada questão em uma pasta com o nome da questão. Ex.: Quest1;
- Todas as Questões devem estar dentro de uma pasta com o nome da atividade. Ex.: Lista1
- Build cada código fonte e deixe o executável na pasta da atividade. Crie uma pasta com o nome `build`;
- Crie um repositório público no GitHub e disponibilize o link para seu professor.
- Use um cabeçalho em cada código fonte. Ex.:

    ```c#
    /*-------------------------------------------------------------------
    Questão 1: Informações do Personagem
    • Contextualização: Em um jogo de RPG, o jogador precisa inserir 
      as informações básicas do personagem antes de começar a aventura.
    • Comando: Crie um programa que receba o nome, idade, nível inicial, 
      classe, e raça do personagem e exiba esses dados no console.
    @Lista: 01 - Lógica de Programação
    @Autor: Chagas Junior
    @Data: 16/08/2024
    ---------------------------------------------------------------------*/
    ```

## Questão 1: Seleção de Armadura

**Contextualização:** Em um jogo de RPG, cada classe de personagem (Guerreiro, Arqueiro, Mago) possui requisitos diferentes para a escolha da armadura ideal. A armadura é considerada ideal se a defesa oferecida for alta o suficiente para a classe e se a penalidade de agilidade for aceitável.

**Comando:** Crie um programa que receba a classe do personagem, o valor de defesa da armadura e a penalidade de agilidade. O programa deve informar se a armadura é adequada ou não para a classe.
- Para o Guerreiro, a defesa deve ser maior que 50 e a penalidade de agilidade menor que 20.
- Para o Arqueiro, a defesa deve ser maior que 30 e a penalidade de agilidade menor que 10.
- Para o Mago, a defesa deve ser maior que 20 e a penalidade de agilidade menor que 40.

**Tabela de Teste:**

| Cenário de Teste                        | Classe   | Defesa | Penalidade de Agilidade | Saída               |
|-----------------------------------------|----------|--------|--------------------------|---------------------|
| Armadura ideal para Guerreiro           | Guerreiro | 60     | 15                       | Armadura adequada   |
| Armadura ideal para Arqueiro            | Arqueiro  | 40     | 5                        | Armadura adequada   |
| Armadura ideal para Mago                | Mago      | 25     | 30                       | Armadura adequada   |
| Armadura não adequada                   | Guerreiro | 40     | 15                       | Armadura não adequada |

## Questão 2: Sistema de Pontuação em Batalha

**Contextualização:** Em um jogo de RPG, o jogador ganha pontos após derrotar inimigos em uma batalha. A pontuação máxima é de 100 pontos, e é determinada pela quantidade de inimigos derrotados, a duração da batalha e se o jogador sofreu danos críticos.

**Comando:** Crie um programa que calcule a pontuação final do jogador. O programa deve receber o número de inimigos derrotados, a duração da batalha em minutos e se o jogador sofreu danos críticos (sim ou não). A pontuação é calculada da seguinte forma:
- 10 pontos para cada inimigo derrotado;
- Subtraia 10 pontos se a batalha durar mais de 5 minutos;
- Subtraia 10 pontos se o jogador sofreu dano crítico.

**Tabela de Teste:**

| Cenário de Teste             | Inimigos Derrotados | Duração da Batalha (min) | Sofreu Danos Crítico | Saída   |
|------------------------------|---------------------|--------------------------|----------------------|---------|
| Pontuação máxima alcançada   | 12                  | 4                        | Não                  | 100 pontos |
| Batalha prolongada           | 8                   | 6                        | Não                  | 80 pontos |
| Sofreu danos críticos        | 15                  | 3                        | Sim                  | 90 pontos |
| Não atingiu a meta           | 10                  | 5                        | Não                  | 100 pontos |

## Questão 3: Loja de Poções

**Contextualização:** Em uma loja de poções mágicas, o jogador pode comprar poções que aumentam sua vida, mana ou resistência. O preço das poções é fixo: Vida custa 10 moedas, Mana custa 15 moedas, e Resistência custa 20 moedas. Dependendo da classe do jogador, há um desconto aplicável.

**Comando:** Crie um programa que receba a classe do jogador (Guerreiro, Mago, Paladino), o tipo de poção (Vida, Mana, Resistência), e a quantidade que deseja comprar. Calcule o preço total das poções, aplicando o desconto correspondente:
- Guerreiro recebe 10% de desconto na compra de poções de Vida.
- Mago recebe 15% de desconto na compra de poções de Mana.
- Paladino recebe 20% de desconto na compra de poções de Resistência.
- Exiba o preço total com e sem desconto.

**Tabela de Teste:**

| Cenário de Teste                          | Classe    | Tipo de Poção | Quantidade | Preço Sem Desconto | Preço Com Desconto |
|-------------------------------------------|-----------|---------------|------------|--------------------|--------------------|
| Guerreiro comprando poções de Vida com desconto | Guerreiro | Vida          | 5          | 50                 | 45                 |
| Mago comprando poções de Mana com desconto | Mago      | Mana          | 4          | 60                 | 51                 |
| Paladino comprando poções de Resistência com desconto | Paladino | Resistência   | 3          | 60                 | 48                 |
| Sem desconto                              | Guerreiro | Mana          | 2          | 30                 | 30                 |

## Questão 4: Decisão de Ataque Especial

**Contextualização:** Durante uma batalha em um jogo de RPG, o jogador pode realizar um ataque especial se tiver mana suficiente, se a vida do inimigo estiver baixa e se o nível do jogador for alto o bastante.

**Comando:** Crie um programa que determine se o jogador deve realizar um ataque especial. O programa deve receber a quantidade de mana do jogador, a vida atual do inimigo em porcentagem e o nível do jogador. As condições para realizar o ataque especial são:
- Mana maior que 30.
- Vida do inimigo menor que 50%.
- Nível do jogador maior que 5.

**Tabela de Testes:**

| Cenário de Teste                   | Mana do Jogador | Vida do Inimigo (%) | Nível do Jogador | Saída                         |
|------------------------------------|-----------------|---------------------|------------------|-------------------------------|
| Ataque especial realizado          | 40              | 40                  | 6                | Ataque Especial realizado     |
| Mana insuficiente                  | 25              | 30                  | 7                | Mana insuficiente             |
| Vida do inimigo muito alta         | 35              | 60                  | 8                | Vida do inimigo muito alta    |
| Nível insuficiente                 | 45              | 40                  | 4                | Nível insuficiente            |

## Questão 5: Resgate no Labirinto

**Contextualização:** Em uma missão de resgate em um jogo, o jogador deve decidir se continua em frente para resgatar um aliado ou recua, considerando a vida restante, o número de armadilhas conhecidas no caminho e a distância do aliado.

**Comando:** Crie um programa que receba a porcentagem de vida do jogador, o número de armadilhas conhecidas no caminho e a distância do aliado em metros. O programa deve decidir se o jogador deve seguir em frente, tentar um resgate rápido, ou recuar, conforme as seguintes condições:
- Se a vida for maior que 50% e as armadilhas forem menores que 3, seguir em frente.
- Se a vida for menor que 50%, as armadilhas forem menores que 2, e a distância do aliado for menor que 10m, tentar resgate rápido.
- Caso contrário, recuar.

**Tabela de Teste:**

| Cenário de Teste                     | Vida (%) | Armadilhas Conhecidas | Distância do Aliado (m) | Saída                     |
|--------------------------------------|----------|-----------------------|--------------------------|---------------------------|
| Seguir em frente                     | 60       | 2                     | 15                       | Seguir em frente          |
| Tentar resgate rápido                | 40       | 1                     | 8                        | Tentar resgate rápido     |
| Recuar por alta quantidade de armadilhas | 30       | 3                     | 20                       | Recuar                    |
| Recuar por risco elevado             | 70       | 4                     | 5                        | Recuar                    |
