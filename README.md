# Diagnóstico de retomada - Teoria da Computação

Esta atividade serve para mapear o que você já domina sobre linguagens formais, autômatos, gramáticas e computabilidade.

Responda individualmente. Use suas palavras. Se usar IA depois da primeira tentativa, registre o uso na seção 7.

## 1. Mapa do que eu lembro

Marque cada tópico como: lembro bem, lembro parcialmente, não lembro, nunca vi ou não tenho certeza.

- alfabeto:LEMBRO BEM
- cadeia:LEMBRO PARCIALMENTE
- linguagem:LEMBRO BEM
- gramática:LEMBRO PARCIALMENTE
- autômato finito:LEMBRO BEM
- linguagem regular:LEMBRO BEM
- linguagem livre de contexto:LEMBRO PARCIALMENTE/NÃO LEMBRO(LEMBRO MUITO POUCO)
- linguagem sensível ao contexto: LEMBRO BEM
- linguagem irrestrita:LEMBRO BEM
- hierarquia de Chomsky:LEMBRO PARCIALMENTE
- computabilidade:NUNCA VI(FALTEI NO DIA DA AULA)
- máquina de Turing:LEMBRO BEM

## 2. Definições com exemplo

Explique, com suas palavras e com um exemplo simples, usando o alfabeto `Sigma = {a, b}`.

1. O que é um alfabeto? Símbolos que existem para serem usados em determinado universo, SIGMA = {a,b}, então somente uma sequência que contenha única e exclusivamente a letra a e a letra b serão aceitas
2. O que é uma cadeia? É qualquer sequência finita de símbolos formados ao juntar as peças de um alfabeto. exemplo: "aabb" "aba" "bbab"
3. O que é uma linguagem? Se trata de um conjunto de cadeias construídas a partir do alfabeto e normalmente apresenta condições, exemplo: apenas cadeias que começam a e terminam com b: "aba" e "aabb"
4. O que é uma gramática? se trata de um molde para criar cadeias

## 3. Linguagens

Considere as linguagens:

```text
L1 = { w em {0,1}* | w termina com 01 }
L2 = { a^n b^n | n >= 0 }
L3 = { a^n b^n c^n | n >= 0 }
```

Para cada linguagem:

1. escreva três palavras que pertencem à linguagem;
L1: 0101,000010, 1010
L2: ab,aabb,aaabbb
L3: abc,aabbcc,aaabbbccc
2. escreva duas palavras que não pertencem;
L1: 10, 010
L2: aab,abb
L3: abcc, abbc
3. diga, se souber, em qual classe ela provavelmente se encaixa;
L1: Linguagem regular
L2: Não tenho certeza mas acredito que Linguagem sensível ao contexto
L3: Linguagem sensível ao contexto
4. explique o motivo em linguagem simples.
L1: Não necessita memória então um automâto finito é capaz de resolver
L2: Necessita memória para contar se os elementos "a" e "b" apresentam a mesma quantidade
L3: Necessita memória para contar se os elementos "a" e "b" apresentam a mesma quantidade

Não há problema em dizer "não sei". Nesse caso, escreva o que te deixou em dúvida.

## 4. Autômato finito

Considere o autômato abaixo, sobre o alfabeto `{0,1}`:

```text
Estados: q0, q1, q2
Estado inicial: q0
Estado final: q2

Transições:
q0 --0--> q1
q0 --1--> q0
q1 --0--> q1
q1 --1--> q2
q2 --0--> q1
q2 --1--> q0
```

Responda:

1. Qual linguagem esse autômato parece reconhecer?
Linguagem regular
2. Execute manualmente as cadeias abaixo e diga se aceita ou rejeita:
   - `01` ACEITA
   - `101` ACEITA
   - `100` REJEITA
   - `1101` ACEITA
   - `111` ACEITA
4. Monte uma tabela curta mostrando o caminho dos estados para pelo menos duas cadeias.
 `01` q0 -> q1, q1 -> q2
 `100` q0 -> q0, q0 -> q1, q1 -> q1
## 5. Gramática

Considere a gramática:

```text
S -> aS
S -> b
```

Responda:

1. Gere cinco cadeias produzidas por essa gramática.
 aab, ab, aaab , aaaaab , aaaaaaaaaaaaaaaaab
2. Descreva a linguagem em palavras.
 não lemmbro ao certo, mas se não me egnano essa gramática vai gerar cadeias que começam em a(não sei dizer se é obrigatório começar com a), e obrigatoriamente devem terminar em b
5. Essa gramática parece regular, livre de contexto ou outra classe? Justifique de forma simples.
 regular, pois não é necessário memória, apenas o último e penúltimo elementos devem ser verificado
## 6. Ponto de dificuldade

Escolha um tópico da lista inicial e escreva:
TÓPICO ESCOLHIDO: 5. Gramática
1. o que você entende dele;
Eu sei oque é por definição
2. onde você se confunde;
Bom, eu nunca implementei ele em um código de nenhuma atividade então não sei como funciona o processo e não lembro muito bem como ele funciona para montar uma cadeia, tipo como funciona "S -> aS", não lembro se é obrigatório passar por ele por exemplo, ou "S -> b" permite uma cadeia só com "b" e por aí vai
3. que tipo de explicação ajudaria: desenho, exemplo, exercício guiado, analogia, prova passo a passo ou lista curta.
lista curta

## 7. Uso de IA, se houver

Se você usou IA depois da primeira tentativa, registre:

```text
Pergunta feita: mandei a print das 4 primeiras questões (tópico 2 inteiro) sem nenhum texto
Resumo da resposta: respondeu cada questão seguida de conceito e exemplo para cada
Como eu verifiquei: honestamente, usei mais para verificar a minha resposta, como garantia para saber se eu lembrava mesmo 
O que eu alterei na minha resposta: nada
O que ainda não entendi: nada :v
```

## Submissão no Moodle

Depois de finalizar, copie no Moodle:

```text
Repositório:
Commit final:
Autoavaliação: nível atual, maior dificuldade e tópico que precisa ser retomado.
```
