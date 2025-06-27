# Guia de Estudos para a Certificação AWS AI Practitioner (AIF-C01)

Olá! Este é um guia de estudos completo e estratégico para a prova **AWS Certified AI Practitioner (AIF-C01)**. Ele está organizado de acordo com os 5 domínios oficiais do exame, com base no "Guia de Estudo Completo – Certificação AWS AI Practitioner".

O objetivo é direcionar seu aprendizado, cobrindo os conceitos, serviços e práticas essenciais para sua aprovação.

---

## Domínio 1: Fundamentos de IA e ML (20% da Prova) 
> Este domínio valida seu conhecimento sobre a terminologia essencial, os diferentes tipos de aprendizado, o ciclo de vida de um projeto de ML e sua capacidade de identificar os serviços da AWS adequados para cada cenário. 
### Tópicos-chave para Estudo:

* **Diferenças Conceituais:**
    * Entenda a relação e as diferenças entre Inteligência Artificial (IA), Machine Learning (ML), Deep Learning (DL) e Ciência de Dados. 
    * Saiba o que caracteriza a IA Generativa (criação de conteúdo novo e original) em comparação com a IA tradicional (análise de dados existentes).  

* **Tipos de Aprendizado de Máquina:**
    * **Supervisionado:** Utiliza dados rotulados (com respostas conhecidas).  
        * **Classificação:** Prever uma categoria (ex: "spam" ou "não spam").  
        * **Regressão:** Prever um valor numérico (ex: o preço de uma casa).  
    * **Não Supervisionado:** Utiliza dados não rotulados para encontrar padrões ocultos.  
        * **Clustering:** Agrupar dados em segmentos (ex: segmentação de clientes).  
        * **Detecção de Anomalias:** Identificar eventos raros ou outliers.  
    * **Aprendizado por Reforço:** Um agente aprende por tentativa e erro, buscando maximizar uma recompensa.  195, 196] O **AWS DeepRacer** é um exemplo prático deste tipo de aprendizado.  

* **Ciclo de Vida de um Projeto de ML:**
    * Conheça todas as etapas, desde a definição do problema até o monitoramento em produção.  
    * Foque em etapas como Preparação e Limpeza de Dados (usando ferramentas como **SageMaker Data Wrangler**   ou **AWS Glue DataBrew**  ), Treinamento, Avaliação, Implantação (Deploy) e Monitoramento.

* **Identificação de Serviços AWS:**
    * **Para construir modelos personalizados:** A resposta principal é o **Amazon SageMaker**, a plataforma completa de ML da AWS.
    * **Para soluções prontas (APIs de IA):**
        * Análise de imagens e vídeos: **Amazon Rekognition** 
        * Entendimento de texto (sentimento, entidades): **Amazon Comprehend**  
        * Criação de chatbots: **Amazon Lex**
        * Tradução de idiomas: **Amazon Translate**
        * Extração de texto e tabelas de documentos: **Amazon Textract** 

---

## Domínio 2: Fundamentos de IA Generativa (24% da Prova) 

> Este é um dos domínios com maior peso. Ele foca nos conceitos específicos de IA Generativa, como funcionam os grandes modelos de linguagem (LLMs) e como interagir com eles. 

### Tópicos-chave para Estudo:

* **Conceitos Fundamentais:**
    * **Modelos Fundacionais (Foundation Models - FMs):** Modelos de grande escala, pré-treinados em vastos volumes de dados, que podem ser adaptados para múltiplas tarefas.  
    * **LLMs (Large Language Models):** O tipo mais comum de FM, focado em tarefas de linguagem, tipicamente com bilhões de parâmetros.  
    * **Embeddings e Tokens:** Entenda como o texto é processado e representado numericamente pelos modelos. 

* **Técnicas e Infraestrutura:**
    * **Prompt Engineering:** A arte de criar entradas (prompts) eficazes para guiar a saída do modelo. 
    * **Infraestrutura para IA Generativa:** Saiba que a AWS oferece hardware especializado como os chips **AWS Trainium** (para treinamento) e **AWS Inferentia** (para inferência), que otimizam custos e performance.  

* **Serviços AWS para IA Generativa:**
    * **Amazon Bedrock:** É o serviço central. Funciona como um hub que oferece acesso a FMs de diversos provedores (como Anthropic, AI21, Meta e da própria AWS) através de uma única API, sem gerenciar infraestrutura.  
    * **Amazon SageMaker JumpStart:** Oferece um catálogo de modelos pré-treinados, incluindo alguns FMs, que podem ser implantados ou ajustados (fine-tuned) rapidamente.

---

## Domínio 3: Aplicações de Modelos Fundacionais (28% da Prova)  

> Este é o domínio de maior peso, focado no uso prático dos FMs. A prova testará seu conhecimento sobre como selecionar, personalizar e avaliar esses grandes modelos.  

### Tópicos-chave para Estudo:

* **Uso e Customização de FMs:**
    * **Critérios de Seleção:** Entenda como escolher o FM mais adequado para uma tarefa.  51]
    * **Ajuste Fino (Fine-Tuning) vs. Prompting:** Saiba a diferença entre usar um modelo como está (zero-shot/few-shot) e adaptá-lo com dados adicionais (fine-tuning).  
    * **Retrieval-Augmented Generation (RAG):** Conceito crucial. É a técnica de conectar um LLM a uma base de dados externa para que ele possa responder perguntas usando informações privadas e atualizadas, sem necessidade de re-treinamento.  

* **Avaliação de Modelos Generativos:**
    * Conheça as métricas usadas para avaliar a qualidade de textos gerados, como **ROUGE** e **BLEU**. 

* **Serviços AWS Relevantes:**
    * **Amazon Bedrock:** Novamente, é o serviço principal para aplicar essas técnicas.  
    * **Bancos de Dados de Vetores (Vector Databases):** Essenciais para implementar a arquitetura RAG. 

---

## Domínio 4: Diretrizes de IA Responsável (14% da Prova)  

> Este domínio aborda os aspectos éticos da IA. É fundamental entender como construir sistemas que sejam justos, transparentes e seguros. 

### Tópicos-chave para Estudo:

* **Princípios de IA Responsável:**
    * **Viés e Justiça (Fairness):** Entenda como o viés pode surgir nos dados ou no modelo, levando a resultados injustos, e a importância de mitigar isso. 
    * **Explicabilidade e Transparência:** Modelos de IA não devem ser "caixas-pretas".  1386] Conheça técnicas como **SHAP** e **LIME** que ajudam a explicar por que um modelo tomou uma decisão.

* **Ferramentas e Recursos da AWS:**
    * **Amazon SageMaker Clarify:** É a principal ferramenta para detectar viés em dados e modelos, e para gerar relatórios de explicabilidade usando SHAP.
    * **SageMaker Model Monitor:** Pode ser usado para monitorar o desvio (drift) de viés em produção.
    * **SageMaker Model Cards:** Servem para documentar informações importantes do modelo, incluindo considerações éticas e de viés.
    * **Amazon Augmented AI (A2I):** Permite integrar revisores humanos no fluxo, um componente chave para a governança em casos sensíveis. 

---

## Domínio 5: Segurança, Conformidade e Governança para Soluções de IA (14% da Prova) 

> Este domínio foca em como proteger os dados e os modelos, garantindo a conformidade com regulações e a boa governança do ciclo de vida da IA. 

### Tópicos-chave para Estudo:

* **Segurança de Dados e Acesso:**
    * **Controle de Acesso:** O **AWS IAM** é fundamental.  56] Use papéis (roles) e políticas para aplicar o princípio do menor privilégio. 
    * **Criptografia:** Proteja os dados em repouso (no S3, por exemplo) e em trânsito. 

* **Monitoramento e Auditoria:**
    * **AWS CloudTrail:** Registra todas as chamadas de API, permitindo auditar "quem fez o quê e quando".
    * **Amazon Macie:** Ajuda a descobrir e proteger dados sensíveis (como PII) armazenados no **Amazon S3**.

* **Governança de Modelos e Dados:**
    * **Ciclo de Vida e Linhagem:** Conhecer a origem dos dados e as versões dos modelos é crucial para a governança.
    * **Conformidade:** Saiba que existem serviços como **AWS Artifact** e **AWS Audit Manager** para ajudar com relatórios de conformidade regulatória.
    * **SageMaker Model Registry:** Essencial para versionar e gerenciar o ciclo de vida dos modelos aprovados para produção.

---

Boa sorte nos seus estudos e sucesso na prova!
