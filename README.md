# 📊 Senai_LLP_ArrayList_Estatistica

![Java](https://img.shields.io/badge/Java-ED8B00?style=flat&logo=openjdk&logoColor=white)
![Status](https://img.shields.io/badge/status-conclu%C3%ADdo-brightgreen)
![Contexto](https://img.shields.io/badge/contexto-acad%C3%AAmico%20SENAI%2FFATESG-blue)

## 📌 Sobre o projeto

Este repositório reúne um conjunto de pequenos programas em Java que calculam medidas estatísticas básicas (média, valor máximo, valor mínimo, desvio padrão e moda) a partir de uma lista de números digitada pelo usuário. Ele foi desenvolvido durante a disciplina de **Linguagem e Lógica de Programação (LLP)** do curso técnico/superior em **Análise e Desenvolvimento de Sistemas do SENAI/FATESG**, como exercício prático sobre estruturas de dados (arrays e coleções) aplicadas a cálculos estatísticos.

## 🎯 Objetivo

Praticar a leitura de dados via console, o armazenamento de valores em arrays/listas e a implementação, "na mão", dos principais algoritmos estatísticos descritivos — sem uso de bibliotecas prontas de estatística — fixando os conceitos de laços de repetição, acumuladores e manipulação de coleções em Java.

## 🛠️ O que foi desenvolvido

Cinco programas independentes, cada um com uma única responsabilidade:

| Arquivo | O que calcula |
|---|---|
| `MediaLista.java` | Média aritmética de uma lista de números digitados pelo usuário. |
| `MaximoLista.java` | O maior valor entre os números informados, comparando item a item. |
| `MinimoLista.java` | O menor valor entre os números informados, comparando item a item. |
| `DesvioPadrao.java` | Média e desvio padrão populacional da lista (raiz quadrada da média dos quadrados dos desvios). |
| `ModaLista.java` | O(s) valor(es) que mais se repete(m) na lista, usando `HashMap` para contar a frequência de cada número. |

## ⚙️ Como funciona

Cada arquivo é um programa Java independente com seu próprio método `main`. O fluxo é sempre parecido:

1. O programa pergunta quantos números serão inseridos (`Scanner.nextInt()`);
2. Os números são lidos um a um, dentro de um laço `for`, e armazenados em um array (`double[]` ou `int[]`);
3. O cálculo estatístico correspondente é feito sobre os valores armazenados;
4. O resultado é exibido no console, formatado com `System.out.printf`.

Para executar qualquer um deles (com o JDK instalado):

```bash
javac MediaLista.java
java MediaLista
```

(substitua `MediaLista` pelo nome do arquivo/classe desejado)

## 💻 Tecnologias utilizadas

- **Java (SE)** — linguagem usada em todos os programas, sem frameworks ou dependências externas.
- **`java.util.Scanner`** — leitura dos valores digitados pelo usuário no terminal.
- **Arrays (`double[]`, `int[]`)** — armazenamento em memória dos números lidos, em `MediaLista`, `DesvioPadrao` e `ModaLista`.
- **`java.util.HashMap`** — em `ModaLista.java`, usado para contar quantas vezes cada número aparece na lista (par chave/valor = número/frequência).
- **`java.util.ArrayList` e `java.util.Collections`** — em `ModaLista.java`, para guardar os valores empatados em frequência máxima (caso de lista multimodal) e obter o maior valor de frequência com `Collections.max`.
- **`Math.pow` e `Math.sqrt`** — usados em `DesvioPadrao.java` para elevar ao quadrado as diferenças e extrair a raiz do resultado final.
- **`String.format` / `printf`** — formatação dos resultados numéricos com duas casas decimais.

## ✅ Principais funcionalidades

- Entrada dinâmica: o usuário define quantos números deseja informar antes de digitá-los.
- Validação simples de quantidade mínima de elementos em alguns dos programas (`MaximoLista`, `MinimoLista`, `DesvioPadrao`).
- Cálculo de cinco medidas estatísticas clássicas de forma independente e didática.
- Tratamento do caso de lista **multimodal** em `ModaLista.java` (quando mais de um valor tem a maior frequência).

## 📁 Estrutura do projeto

```
Senai_LLP_ArrayList_Estatistica/
├── MediaLista.java       # Cálculo da média
├── MaximoLista.java      # Cálculo do valor máximo
├── MinimoLista.java      # Cálculo do valor mínimo
├── DesvioPadrao.java     # Cálculo da média e do desvio padrão
└── ModaLista.java        # Cálculo da moda estatística
```

Cada arquivo é autocontido (não há dependência entre eles), o que reflete a natureza do exercício: uma coleção de pequenos programas para praticar um conceito por vez, em vez de uma aplicação única e integrada.

## 📚 O que foi aprendido

- Diferença entre percorrer um array para achar extremos (máximo/mínimo) versus acumular valores para uma média.
- Implementação manual de uma fórmula estatística (desvio padrão) a partir da sua definição matemática, sem usar bibliotecas prontas.
- Uso de `HashMap` como estrutura de contagem de frequência — uma primeira aproximação prática ao padrão "contar ocorrências" que aparece em muitos problemas de programação.
- Cuidados básicos de validação de entrada (evitar listas vazias ou tamanho inválido).

## 🎓 Contexto acadêmico

Este projeto está entre os **primeiros repositórios publicados no GitHub** por mim durante minha formação em **Análise e Desenvolvimento de Sistemas no SENAI/FATESG**, na disciplina de Linguagem e Lógica de Programação. Ele representa uma etapa inicial da minha evolução como desenvolvedor: o foco aqui é a lógica e a correção dos algoritmos, não a arquitetura de software, testes automatizados ou boas práticas mais avançadas — que vieram em projetos posteriores. Mantenho o repositório como está para documentar esse ponto de partida.

## ⚠️ Observações

- São programas de console simples, sem interface gráfica e sem tratamento de exceções mais robusto (por exemplo, entradas não numéricas podem interromper a execução).
- Não há testes automatizados nem gerenciador de dependências (Maven/Gradle) — cada arquivo é compilado e executado isoladamente, como é comum em exercícios introdutórios de lógica de programação.

## 👤 Autor

**João Pedro Abdala** — estudante de Análise e Desenvolvimento de Sistemas (SENAI/FATESG)
[github.com/joaoabdala05](https://github.com/joaoabdala05)
