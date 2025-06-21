# Guia de Estudos para a Certificação AWS AI Practitioner (AIF-C01)

Olá! Este é um guia de estudos completo e estratégico para a prova **AWS Certified AI Practitioner (AIF-C01)**. Ele está organizado de acordo com os 5 domínios oficiais do exame, com base no "Guia de Estudo Completo – Certificação AWS AI Practitioner".

O objetivo é direcionar seu aprendizado, cobrindo os conceitos, serviços e práticas essenciais para sua aprovação.

---

## [cite_start]Domínio 1: Fundamentos de IA e ML (20% da Prova) [cite: 49]

> [cite_start]Este domínio valida seu conhecimento sobre a terminologia essencial, os diferentes tipos de aprendizado, o ciclo de vida de um projeto de ML e sua capacidade de identificar os serviços da AWS adequados para cada cenário. [cite: 49]

### Tópicos-chave para Estudo:

* **Diferenças Conceituais:**
    * [cite_start]Entenda a relação e as diferenças entre Inteligência Artificial (IA), Machine Learning (ML), Deep Learning (DL) e Ciência de Dados. [cite: 128]
    * [cite_start]Saiba o que caracteriza a IA Generativa (criação de conteúdo novo e original) em comparação com a IA tradicional (análise de dados existentes). [cite: 150, 151]

* **Tipos de Aprendizado de Máquina:**
    * [cite_start]**Supervisionado:** Utiliza dados rotulados (com respostas conhecidas). [cite: 164]
        * [cite_start]**Classificação:** Prever uma categoria (ex: "spam" ou "não spam"). [cite: 168]
        * [cite_start]**Regressão:** Prever um valor numérico (ex: o preço de uma casa). [cite: 170]
    * [cite_start]**Não Supervisionado:** Utiliza dados não rotulados para encontrar padrões ocultos. [cite: 178, 179]
        * [cite_start]**Clustering:** Agrupar dados em segmentos (ex: segmentação de clientes). [cite: 182]
        * [cite_start]**Detecção de Anomalias:** Identificar eventos raros ou outliers. [cite: 184]
    * [cite_start]**Aprendizado por Reforço:** Um agente aprende por tentativa e erro, buscando maximizar uma recompensa. [cite: 195, 196] [cite_start]O **AWS DeepRacer** é um exemplo prático deste tipo de aprendizado. [cite: 204]

* **Ciclo de Vida de um Projeto de ML:**
    * [cite_start]Conheça todas as etapas, desde a definição do problema até o monitoramento em produção. [cite: 211, 213]
    * [cite_start]Foque em etapas como Preparação e Limpeza de Dados (usando ferramentas como **SageMaker Data Wrangler** [cite: 221] [cite_start]ou **AWS Glue DataBrew** [cite: 221]), Treinamento, Avaliação, Implantação (Deploy) e Monitoramento.

* **Identificação de Serviços AWS:**
    * [cite_start]**Para construir modelos personalizados:** A resposta principal é o **Amazon SageMaker**, a plataforma completa de ML da AWS. [cite: 17, 355, 356]
    * **Para soluções prontas (APIs de IA):**
        * [cite_start]Análise de imagens e vídeos: **Amazon Rekognition** [cite: 71, 547]
        * [cite_start]Entendimento de texto (sentimento, entidades): **Amazon Comprehend** [cite: 77, 568]
        * [cite_start]Criação de chatbots: **Amazon Lex** [cite: 72, 591]
        * [cite_start]Tradução de idiomas: **Amazon Translate** [cite: 72, 640]
        * [cite_start]Extração de texto e tabelas de documentos: **Amazon Textract** [cite: 377, 675]

---

## [cite_start]Domínio 2: Fundamentos de IA Generativa (24% da Prova) [cite: 50]

> Este é um dos domínios com maior peso. [cite_start]Ele foca nos conceitos específicos de IA Generativa, como funcionam os grandes modelos de linguagem (LLMs) e como interagir com eles. [cite: 50]

### Tópicos-chave para Estudo:

* **Conceitos Fundamentais:**
    * [cite_start]**Modelos Fundacionais (Foundation Models - FMs):** Modelos de grande escala, pré-treinados em vastos volumes de dados, que podem ser adaptados para múltiplas tarefas. [cite: 334]
    * [cite_start]**LLMs (Large Language Models):** O tipo mais comum de FM, focado em tarefas de linguagem, tipicamente com bilhões de parâmetros. [cite: 336]
    * [cite_start]**Embeddings e Tokens:** Entenda como o texto é processado e representado numericamente pelos modelos. [cite: 50]

* **Técnicas e Infraestrutura:**
    * [cite_start]**Prompt Engineering:** A arte de criar entradas (prompts) eficazes para guiar a saída do modelo. [cite: 50]
    * [cite_start]**Infraestrutura para IA Generativa:** Saiba que a AWS oferece hardware especializado como os chips **AWS Trainium** (para treinamento) e **AWS Inferentia** (para inferência), que otimizam custos e performance. [cite: 359, 362]

* **Serviços AWS para IA Generativa:**
    * **Amazon Bedrock:** É o serviço central. [cite_start]Funciona como um hub que oferece acesso a FMs de diversos provedores (como Anthropic, AI21, Meta e da própria AWS) através de uma única API, sem gerenciar infraestrutura. [cite: 367, 368]
    * [cite_start]**Amazon SageMaker JumpStart:** Oferece um catálogo de modelos pré-treinados, incluindo alguns FMs, que podem ser implantados ou ajustados (fine-tuned) rapidamente. [cite: 370, 371]

---

## [cite_start]Domínio 3: Aplicações de Modelos Fundacionais (28% da Prova) [cite: 51]

> Este é o domínio de maior peso, focado no uso prático dos FMs. [cite_start]A prova testará seu conhecimento sobre como selecionar, personalizar e avaliar esses grandes modelos. [cite: 51]

### Tópicos-chave para Estudo:

* **Uso e Customização de FMs:**
    * [cite_start]**Critérios de Seleção:** Entenda como escolher o FM mais adequado para uma tarefa. [cite: 51]
    * [cite_start]**Ajuste Fino (Fine-Tuning) vs. Prompting:** Saiba a diferença entre usar um modelo como está (zero-shot/few-shot) e adaptá-lo com dados adicionais (fine-tuning). [cite: 51]
    * **Retrieval-Augmented Generation (RAG):** Conceito crucial. [cite_start]É a técnica de conectar um LLM a uma base de dados externa para que ele possa responder perguntas usando informações privadas e atualizadas, sem necessidade de re-treinamento. [cite: 51]

* **Avaliação de Modelos Generativos:**
    * [cite_start]Conheça as métricas usadas para avaliar a qualidade de textos gerados, como **ROUGE** e **BLEU**. [cite: 51]

* **Serviços AWS Relevantes:**
    * [cite_start]**Amazon Bedrock:** Novamente, é o serviço principal para aplicar essas técnicas. [cite: 51]
    * [cite_start]**Bancos de Dados de Vetores (Vector Databases):** Essenciais para implementar a arquitetura RAG. [cite: 51]

---

## [cite_start]Domínio 4: Diretrizes de IA Responsável (14% da Prova) [cite: 52]

> Este domínio aborda os aspectos éticos da IA. [cite_start]É fundamental entender como construir sistemas que sejam justos, transparentes e seguros. [cite: 52, 1363]

### Tópicos-chave para Estudo:

* **Princípios de IA Responsável:**
    * [cite_start]**Viés e Justiça (Fairness):** Entenda como o viés pode surgir nos dados ou no modelo, levando a resultados injustos, e a importância de mitigar isso. [cite: 52, 1367]
    * [cite_start]**Explicabilidade e Transparência:** Modelos de IA não devem ser "caixas-pretas". [cite: 1386] [cite_start]Conheça técnicas como **SHAP** [cite: 54, 1396] [cite_start]e **LIME** [cite: 54, 1390] que ajudam a explicar por que um modelo tomou uma decisão.

* **Ferramentas e Recursos da AWS:**
    * [cite_start]**Amazon SageMaker Clarify:** É a principal ferramenta para detectar viés em dados e modelos, e para gerar relatórios de explicabilidade usando SHAP. [cite: 53, 1380, 1405]
    * [cite_start]**SageMaker Model Monitor:** Pode ser usado para monitorar o desvio (drift) de viés em produção. [cite: 436]
    * [cite_start]**SageMaker Model Cards:** Servem para documentar informações importantes do modelo, incluindo considerações éticas e de viés. [cite: 53, 256]
    * [cite_start]**Amazon Augmented AI (A2I):** Permite integrar revisores humanos no fluxo, um componente chave para a governança em casos sensíveis. [cite: 275, 437]

---

## [cite_start]Domínio 5: Segurança, Conformidade e Governança para Soluções de IA (14% da Prova) [cite: 56]

> [cite_start]Este domínio foca em como proteger os dados e os modelos, garantindo a conformidade com regulações e a boa governança do ciclo de vida da IA. [cite: 56, 57, 58]

### Tópicos-chave para Estudo:

* **Segurança de Dados e Acesso:**
    * [cite_start]**Controle de Acesso:** O **AWS IAM** é fundamental. [cite: 56] [cite_start]Use papéis (roles) e políticas para aplicar o princípio do menor privilégio. [cite: 1534]
    * [cite_start]**Criptografia:** Proteja os dados em repouso (no S3, por exemplo) e em trânsito. [cite: 56, 1416]

* **Monitoramento e Auditoria:**
    * [cite_start]**AWS CloudTrail:** Registra todas as chamadas de API, permitindo auditar "quem fez o quê e quando". [cite: 57, 1516]
    * [cite_start]**Amazon Macie:** Ajuda a descobrir e proteger dados sensíveis (como PII) armazenados no **Amazon S3**. [cite: 56, 1427]

* **Governança de Modelos e Dados:**
    * [cite_start]**Ciclo de Vida e Linhagem:** Conhecer a origem dos dados e as versões dos modelos é crucial para a governança. [cite: 57]
    * [cite_start]**Conformidade:** Saiba que existem serviços como **AWS Artifact** e **AWS Audit Manager** para ajudar com relatórios de conformidade regulatória. [cite: 56]
    * [cite_start]**SageMaker Model Registry:** Essencial para versionar e gerenciar o ciclo de vida dos modelos aprovados para produção. [cite: 256]

---

Boa sorte nos seus estudos e sucesso na prova!
