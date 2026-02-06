# **Guia: Como Criar Documentações de Automação no GitHub (Padrão Pareto)**

> Este guia estabelece o padrão para a criação de documentações de automação na organização Pareto-Group-BR. O objetivo é garantir que todos os projetos sejam claros, replicáveis, sustentáveis e fáceis de entender.

---

## 📚 Índice

1.  [**Filosofia Principal**](#1-filosofia-principal)
2.  [**Estrutura e Nomenclatura: A Fundação**](#2-estrutura-e-nomenclatura-a-fundação)
    *   [2.1. Padrão de Nomenclatura](#21-padrão-de-nomenclatura)
    *   [2.2. Criação do Repositório no GitHub](#22-criação-do-repositório-no-github)
    *   [2.3. Estrutura de Arquivos Padrão](#23-estrutura-de-arquivos-padrão)
3.  [**O Coração da Documentação: `README.md`**](#3-o-coração-da-documentação-readmemd)
4.  [**A Documentação Técnica: `Fluxo.md` ou `Detalhamento_Técnico.md`**](#4-a-documentação-técnica-fluxonmd)
5.  [**A Inteligência da Automação: `Agentes_de_IA.md`**](#5-a-inteligência-da-automação-agentes_de_iamd)
6.  [**Boas Práticas e Manutenção Contínua**](#6-boas-práticas-e-manutenção-contínua)
    *   [6.1. Use Versionamento com Tags e Releases](#61-use-versionamento-com-tags-e-releases)
    *   [6.2. Mantenha a Documentação Viva](#62-mantenha-a-documentação-viva)

---

## **1. Filosofia Principal**

Uma automação só tem valor a longo prazo se for compreensível e passível de manutenção. A documentação não é uma tarefa secundária, mas uma parte integral do processo de desenvolvimento. Siga este guia para garantir que seu trabalho seja profissional e duradouro.

Além disso, tenha em mente que toda automação deve ser "templatizável", ou seja, ter uma forma para se tornar replicável por outro usuário. E, a melhor forma de permitir uma replicação mais ágil e simples é criando uma documentação completa de sua automação, seguindo os passos abaixo.

---

## **2. Estrutura e Nomenclatura: A Fundação**

Antes de escrever a primeira linha, a estrutura do repositório deve ser definida corretamente.

### **2.1. Padrão de Nomenclatura**

A consistência é a chave para a organização.

*   **Repositório:** O nome deve ser conciso e descrever a automação. Use letras minúsculas e hifens. Se for uma versão específica, inclua no final.
    *   **Exemplo:** `content-spark-v1`, `lead-enrichment-automation`
*   **Pastas Internas:** Se a automação tiver variações (ex: fluxos para clientes diferentes ou com objetivos distintos), crie pastas para separá-las.
    *   **Exemplo:** `ORIGINAIS`, `SUGESTOES`, `CLIENTE_A`

### **2.2. Criação do Repositório no GitHub**

1.  **Acesse a Organização:** Navegue até [Pareto-Group-BR](https://github.com/Pareto-Group-BR).
    *   *Caso não seja membro, peça a um administrador para lhe adicionar.*
2.  **Crie um Novo Repositório:**
    *   Clique no botão verde **"New"**.
    *   **Nome:** Use o padrão de nomenclatura definido acima.
    *   **Descrição:** Adicione uma frase que resuma o objetivo da automação.
    *   **Visibilidade:** **Public**.
    *   **Inicialização:** Marque a opção **"Add a README file"**.

<img width="1354" height="388" alt="image" src="https://github.com/user-attachments/assets/8e367620-bb03-43ef-8ca3-81d4f6c87db2" />

<img width="700" height="643" alt="image" src="https://github.com/user-attachments/assets/f95738d9-ae9e-481a-9eec-ef53acc343dc" />


### **2.3. Estrutura de Arquivos Padrão**

Dentro do repositório, cada pasta de variação de fluxo deve conter obrigatoriamente três arquivos, como demonstrado na imagem de exemplo:

![Estrutura de arquivos no GitHub](https://cdn.tess.im/assets/uploads/90067587-0306-4dc2-987a-ec463eb3c148.png)

1.  `README.md`: O manual de operação e porta de entrada da automação.
2.  `Fluxo_N8N.md`: O detalhamento técnico do workflow. (O nome pode variar para `Fluxo_Make.md`, `Fluxo_Zapier.md`, etc.).
3.  `Agentes_de_IA.md`: A documentação de todos os agentes de IA utilizados.

Para adicionar um novo arquivi, clique em "Add file" e depois em "Create new file".

<img width="838" height="268" alt="image" src="https://github.com/user-attachments/assets/ac1219e9-de3d-45ce-b436-ae6c7caab181" />

> Para que a formatação em Markdown funcione, é preciso que o **NOME do seu arquivo termine sempre com ".md"**.

> Lembre-se de sempre adicionar um **Índice (Sumário)** em cada arquivo de sua documentação.

---

### **3. O Coração da Documentação: `README.md`**

Este é o arquivo central. Ele serve como um guia completo para o usuário, desde a visão geral até a replicação, contendo links para os arquivos mais detalhados (como o Fluxo e os Agentes de IA).

**Seções Obrigatórias:**

*   **Visão Geral e Objetivo:** O que a automação faz, qual problema resolve e qual o resultado final.
*   **Diagrama Visual do Fluxo:** **Essencial.** Insira uma imagem de um diagrama de alto nível que mostre as principais fases da automação (ex: Planilha -> N8N -> Tess AI -> Google Drive -> Notificação). Isso proporciona um entendimento imediato do processo.
*   **Exemplos de Saída da Automação (NOVO):** Mostre o resultado final! Esta seção tangibiliza o que a automação produz.
    *   **O que incluir:**
        *   **Imagens ou GIFs:** Adicione screenshots ou GIFs do produto final (ex: as imagens do carrossel gerado, um print da linha preenchida na planilha, o email de notificação).
        *   **Links:** Se os artefatos são salvos em algum lugar (como uma pasta no Google Drive), adicione um link para a pasta de exemplos.
        *   **Descrição:** Explique brevemente o que cada exemplo representa.
    *   **Objetivo:** Permitir que o usuário veja a qualidade e o formato do resultado antes mesmo de rodar ou replicar a automação.
*   **Manual de Operação:**
    *   **Pré-requisitos:** Liste tudo que o usuário precisa para usar a automação.
    *   **O Centro de Comando:** Explique como interagir com a automação (ex: preencher uma linha em uma Planilha Google).
*   **Arquitetura e Ferramentas:** Liste todas as plataformas e tecnologias envolvidas.
*   **Passo a Passo para Replicar o Fluxo:** Um guia detalhado para que outra pessoa possa configurar a mesma automação em seu próprio ambiente.
*   **Links e Recursos:** Links diretos para os arquivos `Fluxo_N8N.md` e `Agentes_de_IA.md` dentro do repositório.

---

## **4. A Documentação Técnica: `Fluxo.md` ou `Detalhamento_Técnico**

Este é o blueprint técnico do seu workflow.

**Seções Obrigatórias:**

*   **Visão Geral da Arquitetura:** Um resumo técnico do funcionamento do fluxo ou da plataforma desenvolvida (caso utilize uma integração externa, como *Lovable*).
*   **Diagrama Detalhado do Fluxo:** Insira um diagrama (pode ser criado em formato .mermaid) que mostre os nós principais e suas conexões dentro da plataforma de integração. Uma boa prática é separar o fluxo por FASES, de modo que facilite o entendimento por parte do usuário. Essas mesmas fases serão descritas na seção de Fluxo, com os nós (ou etapas), APIs e credenciais necessárias.
*   **Resumo de APIs, Plataformas e Credenciais:** Um checklist crucial para o usuário.

| Serviço/API | Tipo de Autenticação | Plataforma |
| :--- | :--- | :--- |
| Google Sheets API | OAuth2 | Google Workspace |
| Google Drive API | OAuth2 | Google Workspace |
| Tess AI API | Bearer Token | Tess AI |
| HTML/CSS-to-Image API | API Key | HTML/CSS-to-Image |

*   **Detalhamento do Fluxo por Fases:** Descreva todas as fases da automação e cada nó ou etapa importante contida, informando seu tipo, descrição, e configurações principais. Adicione prints de tela que mostrem essas fases descritas. Caso a automação tenha sido desenvolvida em uma plataforma externa cntendo uma interface (como a *Lovable*), é importante trazer como está configurada e pré-requisitos necessários, permitindo a repliicação.
*   **Link para Download do Arquivo do Fluxo (se existir):**
    1.  **Sanitização Obrigatória:** Caso o seu fluxo tenha sido desenvolvido em uma plataforma integradora (Make, N8N, Zapier), baixe o arquivo contendo as etapas do fluxo. Envie este arquivo (`.json`) para o agente de IA [Anonimizador/Sanitizador de JSON da Tess](https://tess.im/pt-BR/dashboard/user/ai/chat/ai-chat/anonimizadorsanitizador-de-json-para-documentacao-HfUS2D) para remover todas as credenciais, tokens e chaves de API. Gere, no próprio agente de IA, um link público deste novo JSON sanitizado.
    2.  **Hospedagem:** Salve o conteúdo sanitizado em um novo arquivo `.json` (o próprio gerado pela TESS) e faça o upload para o mesmo diretório no GitHub.
    3.  **Link:** Adicione o link de download para este arquivo sanitizado.

---

## **5. A Inteligência da Automação: `Agentes_de_IA.md`**

Documentar os "cérebros" da automação é fundamental para sua replicação e evolução.

**Para cada agente de IA, inclua:**

*   **ID do Agente e Link Público:**
    *   **Boas Práticas:** Nas configurações de compartilhamento do agente na Tess AI, **ative a opção "Permitir que outros usuários clonem este agente"**. Isso permite que qualquer pessoa crie uma cópia exata no próprio workspace com um único clique, acelerando drasticamente a replicação.
*   **Configurações do Agente:** LLM, Temperatura, Ferramentas, etc.
*   **Descrição Profissional:** Qual é o "cargo" do agente (ex: "Diretor de Criação", "Pesquisador Especialista").
*   **Prompt Completo:** Cole o prompt exato dentro de um bloco de código Markdown para preservar a formatação. Caso haja algum AI Step (passos intermediários dentro do seu prompt), deixe isso claro e documentado, trazendo os LLMs ou ferramentas usadas e o prompt.
*   **Prints de Exemplo:** Cole prints mostrando a configuração do seu agente na plataforma de IA utilizada.
  
---

## **6. Boas Práticas e Manutenção Contínua**

Para elevar a qualidade e a longevidade da sua documentação:

### **6.1. Use Versionamento com Tags e Releases**

Não confie apenas no histórico de commits. Quando uma versão estável da sua automação for concluída ou atualizada significativamente:

1.  **Vá para a página inicial do seu repositório.**
2.  **Clique em "Releases" na barra lateral direita.**
3.  **Clique em "Draft a new release".**
4.  **Crie uma tag:** Use versionamento semântico (ex: `v1.0.0`, `v1.1.0`).
5.  **Dê um título para a Release** (ex: "Versão 1.0 - Lançamento Inicial").
6.  **Descreva as mudanças:** O que foi adicionado, corrigido ou alterado nesta versão.
7.  **Publique a release.**

**Por que isso é importante?** Releases criam um "ponto na história" permanente e imutável do seu projeto, facilitando o acompanhamento de mudanças e a referência a versões anteriores.

### **6.2. Mantenha a Documentação Viva**

Uma documentação desatualizada dificulta o trabalho de quem irá fazer a manutenção e de quem irá replicá-la. Crie o hábito: **mudou a automação, atualize a documentação.** A mudança só está "concluída" quando a documentação reflete o novo estado.
