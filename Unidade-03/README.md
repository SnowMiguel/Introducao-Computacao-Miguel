# 🧊 SafeDrop AI: Logística Preditiva de Cadeia de Frio para Vacinas e Medicamentos de Alto Custo

> **DESAFIO INDIVIDUAL - AULA 08**
> 
> **Disciplina:** Introdução à Computação  
> **Curso:** Engenharia de Software (CEUB)  
> **Profa.:** Kadidja Valéria  
> **Aluno/CEO:** Miguel M. Neves  

Bem-vindo ao repositório do Desafio Individual da Aula 08. Este projeto apresenta a modelagem de negócios e a arquitetura de sistemas de informação da **SafeDrop AI**, uma startup projetada sob a ótica de que o dado é o ativo estratégico mais valioso para solucionar problemas complexos da sociedade.

A fundamentação teórica deste projeto apoia-se estritamente nos conceitos discutidos nos materiais de aula da disciplina, em especial os documentos `Dados_Informacao_Conhecimento.pdf` e `Aula08_Parte1_Entendendo o dado.pdf`.

---

## 1. Problema e Dados (A Escolha do Caos)

### 🚨 O Problema Real
A preservação da integridade de termolábeis (vacinas, insumos biológicos e medicamentos de alto custo) é um dos maiores desafios da saúde pública e privada no Brasil. Estima-se que **até 25% das vacinas cheguem ao seu destino final com algum nível de degradação** devido a falhas de temperatura na cadeia de frio.

O "caos" logístico brasileiro — composto por malhas rodoviárias precárias, extremos de temperatura climática e atrasos operacionais — gera desperdício de milhões de reais e coloca vidas em risco.

### 📥 Coleta de Dados Brutos (O Ponto de Partida)
Como estabelecido em *Aula08_Parte1_Entendendo o dado.pdf*, o Dado representa o fato bruto e isolado, isento de contexto e interpretação. Para a SafeDrop AI, nossos "elementos de entrada" consistem em registros soltos de telemetria coletados em tempo real ao longo da jornada logística.

Para mitigar o risco do paradoxo **GIGO (Garbage In, Garbage Out)**, detalhado em *Dados_Informacao_Conhecimento.pdf*, implementamos uma rigorosa classificação e mapeamento de integridade na nossa camada de captação de dados:

| Dado Bruto (Input) | Origem do Dado | Tipo | Pilar de Valor Assegurado |
| :--- | :--- | :--- | :--- |
| **Temperatura e Umidade** | Sensores IoT via rede celular/LoRaWAN | Estruturado (Time-Series / Float) | **Precisão:** Sensores calibrados evitam medições falsas. |
| **Impacto (G-force)** | Acelerômetro do sensor IoT | Estruturado (Time-Series / Float) | **Confiabilidade:** Medição contínua sem interrupções. |
| **Coordenadas GPS** | Rastreador veicular e sensor IoT | Estruturado (Geospatial / JSON) | **Integridade:** Dados completos de latitude e longitude. |
| **Previsão do Tempo** | API externa (ex: OpenWeather) | Estruturado (JSON) | **Oportunidade:** Dados obtidos no exato momento da rota. |
| **Condições de Tráfego** | API de tráfego (ex: Google Maps) | Estruturado (JSON) | **Relevância:** Essencial para calcular o tempo estimado de chegada (ETA). |
| **Registros de Ocorrências** | Boletins públicos e feed de notícias | Não Estruturado (Texto Livre) | **Flexibilidade:** Convertido em dados de risco regional. |
| **Ficha Técnica da Carga**| ERP do laboratório ou hospital | Estruturado (Relacional / SQL) | **Segurança:** Acesso blindado de ponta a ponta. |

---

## 2. Processamento (O Sistema)

Como preconiza a literatura, um Sistema de Computação é sustentado por três pilares: Hardware, Software e Dados. A SafeDrop AI orquestra esses componentes para realizar a jornada de transformação digital da entrada bruta à saída inteligente.

> `[Coleta (MQTT/Kafka)] ──> [Armazenamento (InfluxDB/Postgres)] ──> [Processamento (Flink)] ──> [Análise / IA (Newton)]`

### ⚙️ O Fluxo de Engenharia de Sistemas

* **Coleta (Ingestão/Hardware & Software):** Os sensores IoT (hardware de telemetria) transmitem pacotes leves via protocolo MQTT para um broker escalável Apache Kafka (software de mensageria).
* **Armazenamento (Bancos de Dados):** Dados de séries temporais rápidos e contínuos são persistidos no InfluxDB (banco NoSQL de time-series). Dados estruturados relacionais (cadastro de cargas, hospitais e usuários) são salvos no PostgreSQL.
* **Processamento (Contextualização):** O motor Apache Flink limpa, valida e contextualiza os dados a cada ciclo de transmissão. Esta etapa é o nosso principal filtro contra o *Garbage In, Garbage Out*, garantindo que dados ruidosos ou corrompidos não estraguem a análise preditiva.
* **Análise e Inteligência:** Transformamos o dado bruto em Informação estruturada. Aplicamos um modelo de degradação termodinâmica baseado na adaptação da Lei do Resfriamento de Newton para calcular a perda de eficiência da embalagem em tempo real:

$$T(t) = T_{amb} + (T_i - T_{amb}) \cdot e^{-\alpha t}$$

**Onde:**
* $T(t)$ é a temperatura prevista no tempo $t$.
* $T_{amb}$ é a temperatura ambiente externa prevista para as coordenadas atuais e futuras da rota.
* $T_i$ é a última temperatura interna registrada da vacina pelo sensor IoT.
* $\alpha$ é o coeficiente de isolamento térmico da embalagem específica utilizada.

---

## 3. Informação e Conhecimento (A Transformação)

De acordo com o funil de transformação apresentado em *Dados_Informacao_Conhecimento.pdf*, a transição de Informação para Conhecimento exige uma síntese analítica (frequentemente humana ou, neste caso, auxiliada por IA preditiva).

Fazendo uma analogia ao clássico exemplo clínico de febre abordado em aula (onde o dado isolado de $39^\circ\text{C}$ ganha contexto temporal de febre e gera o conhecimento para administrar um antitérmico), o nosso sistema executa uma "refinaria de dados" contínua:

### 🧠 Descobertas Geradas pelo Sistema de Conhecimento
* 📊 **Padrões:** Identificação de que as embalagens térmicas do lote $L_{302}$ perdem eficiência térmica 15% mais rápido quando expostas a vibrações mecânicas contínuas superiores a $1.5\text{ g}$ (relação entre a suspensão deteriorada do veículo ou asfalto ruim com a integridade do isolamento a vácuo).
* 📈 **Tendências:** Detecção de que rotas que trafegam pelo Centro-Oeste entre as 11:00h e as 14:00h sofrem desvios de temperatura rápidos devido ao calor irradiado pelo asfalto em caminhões sem baú refrigerado.
* 🔮 **Previsões:** Estimativa matemática exata do tempo de autonomia restante da embalagem térmica (ex: *"Esta carga de vacinas de poliomielite perderá a refrigeração de segurança em 42 minutos devido ao congestionamento de 3.2 km detectado na BR-116"*).

O usuário deixa de ser um mero visualizador de relatórios passivos e passa a ter acesso a insights preditivos automatizados.

---

## 4. Decisão e Valor (A Decisão)

O valor real de um sistema de informação não reside em sua sofisticação técnica, mas na sua capacidade de orientar ações práticas e tomadas de decisão inteligentes.

### ⚡ Decisões Habilitadas pela SafeDrop AI
* **Redirecionamento Dinâmico de Emergência:** Caso o modelo termodinâmico estime uma quebra de barreira térmica antes do destino final, o sistema recalcula e sugere a rota para um hospital parceiro mais próximo para salvar o lote de medicamentos.
* **Substituição Preventiva de Elementos Frios (Gelox):** Notificação automática ao motorista via aplicativo parceiro, indicando o ponto de parada e troca de gelo ideal antes do aquecimento do insumo biológico.
* **Bloqueio de Lote Automatizado via Integração ERP:** Se houver uma violação térmica irreversível por mais de 30 minutos, o sistema dispara um gatilho direto para o banco de dados do hospital de destino para bloquear automaticamente o lote, impedindo que uma vacina ineficaz seja aplicada em um paciente.

### 💎 Valor de Negócio Gerado (Mapeado nos 10 Pilares da Informação)
* 📉 **Redução de Custos (Retorno):** Diminuição de até 90% no descarte de medicamentos termolábeis de alto custo e redução direta nas apólices de seguro de carga.
* 🚀 **Aumento de Eficiência (Usabilidade e Simplicidade):** Automatização de relatórios de conformidade térmica para auditorias da Anvisa, eliminando anotações manuais em papel e o erro humano.
* 🎯 **Personalização (Flexibilidade):** Recomendação inteligente da embalagem e quantidade exata de gelo necessária para cada rota específica com base na previsão climática, evitando desperdício de peso e custos logísticos extras.
* 💡 **Inovação:** Criação de um selo de *"Segurança Térmica Garantida por IA"*, agregando valor de marca para laboratórios farmacêuticos e distribuidoras.

---

## 5. Representação (Mapa Conceitual do Sistema)

Abaixo é apresentado o mapa conceitual visual que integra as fases de processamento do dado, a cadeia clássica de sistemas de computação (Entrada, Processamento, Saída e Feedback) e a escala de valor corporativo.

```mermaid
graph TD
    %% Estilos de Cor Acessíveis (Contraste alto para Dark/Light mode no GitHub)
    classDef dado fill:#E8F0FE,stroke:#1A73E8,stroke-width:2px,color:#202124;
    classDef proc fill:#FCE8E6,stroke:#D93025,stroke-width:2px,color:#202124;
    classDef info fill:#E6F4EA,stroke:#1E8E3E,stroke-width:2px,color:#202124;
    classDef con fill:#FEF7E0,stroke:#F9AB00,stroke-width:2px,color:#202124;
    classDef dec fill:#F3E8FD,stroke:#9334E6,stroke-width:2px,color:#202124;
    classDef val fill:#E4F7FB,stroke:#12B5CB,stroke-width:2px,color:#202124;

    %% Elementos de Dados (Entradas)
    subgraph ENTRADA [Elementos de Entrada - Dados Brutos]
        D1[Temperatura / Umidade]:::dado
        D2[GPS / Velocidade]:::dado
        D3[APIs externas de Clima/Tráfego]:::dado
        D4[Cadastro da Carga & ERP]:::dado
    end

    %% Processamento (O Sistema)
    subgraph PROCESSAMENTO [Elementos de Processamento]
        P1[Ingestão MQTT / Kafka]:::proc
        P2[Banco de Dados PostgreSQL / InfluxDB]:::proc
        P3[Modelagem Termodinâmica / Regressão]:::proc
    end

    ENTRADA --> P1
    P1 --> P2
    P2 --> P3

    %% Informação (Saídas Iniciais)
    subgraph SAIDA [Elementos de Saída - Informação Contextualizada]
        I1[Dashboard de Monitoramento em Tempo Real]:::info
        I2[Cálculo de Curva de Aquecimento]:::info
        I3[Alertas de Desvios de Temperatura]:::info
    end

    P3 --> SAIDA

    %% Conhecimento
    subgraph CONHECIMENTO [Síntese e Análise Preditiva]
        C1[Previsão de Tempo de Autonomia Restante]:::con
        C2[Associação entre Rota, Clima e Perda Térmica]:::con
    end

    I2 --> C1
    I3 --> C2

    %% Decisão
    subgraph DECISAO [Ação Prática]
        Dec1[Rota Alternativa Dinâmica]:::dec
        Dec2[Alerta de Troca de Gelox ao Motorista]:::dec
        Dec3[Bloqueio Automático de Lote Danificado]:::dec
    end

    C1 --> Dec1
    C1 --> Dec2
    C2 --> Dec3

    %% Valor Gerado
    subgraph VALOR [Impacto de Negócio]
        V1[Eficiência: Zero Desperdício de Insumos]:::val
        V2[Economia: Redução de Custos Logísticos]:::val
        V3[Inovação: Garantia de Qualidade da Vacina]:::val
    end

    Dec1 --> V1
    Dec2 --> V2
    Dec3 --> V3

    %% Feedback Loop
    subgraph FEEDBACK [Feedback e Aprendizado de Máquina]
        F1[Ajuste dos Coeficientes do Modelo Térmico]:::proc
    end

    V1 -.-> F1
    F1 -.-> P3
