# Atividades Práticas e Avaliativas — Introdução à Computação 💻

Este repositório centraliza as diretrizes, enunciados e modelos de entrega para as atividades práticas e o trabalho em grupo desenvolvidos na disciplina de **Introdução à Computação** do curso de Engenharia de Software, sob a orientação da **Professora Kadidja Valéria**.

---

## 🛑 ATIVIDADE 1: A Evolução do Hardware

### 1. Objetivo
Investigar a evolução técnica dos componentes internos do computador e consolidar o conhecimento sobre a arquitetura básica (ULA, UC, Memória e Periféricos) por meio de uma comparação entre máquinas históricas e a tecnologia atual.

### 2. Materiais de Apoio
* **Acervo Online:** [Computer History Museum (CHM)](https://www.computerhistory.org/)
* **Documentário:** Trechos de *Triumph of the Nerds* (1996)
* **Bibliografia:** Monteiro (2015) ou Tanenbaum (2013)
* **Material Didático:** IMD – Instituto Metrópole Digital. *Material Didático – Arquitetura de Computadores*. Natal: UFRN, 2026. Disponível em: <https://materialpublic.imd.ufrn.br/curso/disciplina/5/14>.

### 3. Escopo da Investigação
Cada aluno ou grupo deve escolher um artefato histórico do acervo do museu (ex: ENIAC, Apple I, Cray-1 ou a calculadora de Babbage) e identificar os seguintes eixos:

* **Processamento:** Como eram executadas as operações lógicas e aritméticas (ULA) e como o fluxo era coordenado (Unidade de Controle).
* **Armazenamento:** Qual era o tipo e a capacidade real da memória e dos registradores da época.
* **Interface:** Quais eram os periféricos de entrada e saída utilizados para a interação.
* **Comparação:** Relacionar esses dados técnicos com um hardware moderno equivalente (ex: um processador atual ou um smartphone).

### ⚙️ Instruções para Entrega no GitHub

#### Passo 1: Criação do Repositório
* Crie um repositório público com a nomenclatura: `Introducao-Computacao-Hardware-NomeDoAluno`.
* O repositório deve obrigatoriamente conter um arquivo chamado `README.md`.

#### Passo 2: Estrutura do Arquivo `README.md`
O relatório da investigação deve ser estruturado em Markdown dentro do arquivo principal contendo:
1. **Título da Atividade:** Investigação de Hardware: `[Nome da Máquina Escolhida]`.
2. **Descrição do Artefato:** Breve histórico do componente ou máquina escolhida no acervo do CHM.
3. **Análise Técnica:** Tabela comparativa detalhada entre o hardware histórico e o moderno (considerando ULA, Memória e Periféricos).
4. **Imagens:** Link ou inserção de imagens do artefato pesquisado (disponíveis no site do museu).
5. **Referências:** Citação das fontes utilizadas (links do museu e bibliografia do plano de ensino).

#### Passo 3: Submissão
* Garanta que o repositório está configurado como **Público**.
* Envie o link do repositório através da plataforma oficial indicada pela professora (conforme o cronograma da Unidade 2).

---

## 🛑 ATIVIDADE 2: Dispositivos de Entrada e Saída (E/S)

### 1. Objetivo
Compreender o papel fundamental dos dispositivos de entrada e saída em um sistema computacional e relacioná-los com situações práticas e reais do cotidiano.

### 2. Enunciado da Atividade

#### Parte 1 – Classificação
Liste **cinco dispositivos** que você utiliza no seu dia a dia e classifique-os em uma das três categorias abaixo:
* **Entrada:** Componentes que traduzem a intenção humana em sinais binários.
* **Saída:** Componentes que traduzem o processamento binário em percepção humana.
* **Entrada/Saída (E/S):** Componentes híbridos que realizam o tráfego bidirecional de dados.

#### Parte 2 – Associação
Explique, em até **duas frases por item**, como cada um dos cinco dispositivos escolhidos se conecta ao sistema operacional (SO) e qual é a sua função principal.

> 💡 **Modelos de formato esperado:**
> * **Teclado (Entrada):** Envia sinais elétricos ao SO, que os interpreta como caracteres digitados.
> * **Monitor (Saída):** Recebe sinais de vídeo do SO e os traduz em imagens visíveis ao usuário.

#### Parte 3 – Reflexão
Responda de forma sucinta às seguintes questões:
1. O que aconteceria se não houvesse dispositivos de saída em um computador?
2. Por que os dispositivos híbridos (como *pen drives* e placas de rede) são essenciais para a comunicação entre sistemas na atualidade?

### ⚙️ Instruções para Entrega

* **Formato do Arquivo:** Escreva e salve suas respostas em um arquivo com formato `.doc`.
* **Nomenclatura Obrigatória:** Nomeie o arquivo exatamente como `Atividade_DispositivosES_16-03.doc`.
* **Local de Envio:** Realize o *commit* e *push* do arquivo no repositório da disciplina, obrigatoriamente dentro da pasta raiz `Atividades/`.

---

## 🛑 TRABALHO EM GRUPO: Seminário de Sistemas Operacionais Modernos

### 1. Objetivo do Trabalho
A missão consiste em realizar uma investigação técnica aprofundada sobre um ecossistema de Sistema Operacional (SO) específico. O objetivo é analisar sua arquitetura, evolução e impacto no mercado sob a ótica de engenharia.

### 2. Formato e Dinâmica
* **Formação:** Grupos de 4 a 5 alunos.
* **Tempo de Apresentação:** De 5 a 7 minutos por grupo (estilo *Pit Stop*, curto e direto).
* **Referência Inicial:** Artigo da Alura e materiais de apoio recomendados em sala.

#### 🗺️ Ecossistemas Alvos para Escolha
Cada grupo deve selecionar uma das seguintes vertentes para investigar:
* Windows
* Linux
* macOS
* Android
* iOS
* Unix

### 3. Arquitetura e Roteiro da Apresentação (Gabarito Visual)
O seminário deve ser estruturado utilizando como base o arquivo `AULA6SISTEMASOPERACIONAIS.pdf`, seguindo rigorosamente os 5 pilares do template do aluno:

1. **Histórico e Evolução:** Mapeamento da linha do tempo, identificando o ano de criação, fundadores e a "versão marco" (aquela que mudou os rumos do mercado).
2. **Arquitetura e Características:** Identificação do modelo de construção do núcleo (*kernel*) — Monolítico, Micronúcleo ou Híbrido —, além do nível de isolamento e segurança nativa do sistema.
3. **Ecossistema e Dispositivos:** Definição dos segmentos onde o SO domina (Desktops, Smartphones, Servidores/Nuvem ou Embarcados) e a estimativa do seu *market share* atual.
4. **Vantagens e Limitações:** Análise crítica de pontos como código aberto, facilidade de uso, fragmentação, custos de licença e barreiras de ecossistema (*lock-in*).
5. **Casos de Uso Prático:** Exemplos do mundo real de quem depende desse SO para funcionar, divididos explicitamente entre o Usuário Comum (gamers, estudantes) e o Mundo Corporativo (datacenters, hospitais, agências espaciais).

### 🧠 Rodada de Sabatina (Defesa Técnica)
Após cada apresentação, o grupo passará por perguntas rápidas de prontidão conduzidas pela professora. Estejam prontos para defender o ecossistema sob as seguintes perspectivas:
* *"Qual é o maior gargalo técnico desse sistema hoje?"*
* *"Por que um desenvolvedor escolheria este SO e não o concorrente direto?"*
* *"Como esse sistema gerencia a segurança do usuário final?"*

### 📐 Critérios de Avaliação

A banca avaliará o desempenho com base em quatro eixos principais:

| Critério | Descrição |
| :--- | :--- |
| **Clareza** | Capacidade de traduzir conceitos complexos de hardware e software de forma simples. |
| **Profundidade** | Ir além do básico (ir além da Wikipédia) e empregar termos técnicos de forma correta. |
| **Organização** | Respeito estrito ao tempo limite estabelecido e manutenção de uma linha lógica coerente. |
| **Participação** | Colaboração mútua de todos os membros e domínio visível do tema por todo o grupo. |

### ⚙️ Entregável Obrigatório
Além da apresentação em grupo, há um componente individual que deve ser enviado:

* **O que entregar:** Resumo Individual em formato digital de exatamente **1 página (A4)**.
* **Conteúdo:** Destacar o Sistema Operacional estudado pelo seu respectivo grupo e sintetizar os principais aprendizados, conclusões e reflexões gerados pela atividade.
