# 🛠️ Hub de Ferramentas Operacionais

Uma suíte web leve, ágil e centralizada para otimização de processos de e-commerce, cadastro de produtos no ERP SAP, formatação padronizada de anúncios, geração de descrições com IA e gestão de fluxo de trabalho (Kanban).

🚀 **Acesse o projeto online:** [https://dgmarques-br.github.io/Hub-Ferramentas/](https://dgmarques-br.github.io/Hub-Ferramentas/)

---

## 📌 Sobre o Projeto

O **Hub de Ferramentas Operacionais** foi desenvolvido para resolver problemas recorrentes da rotina comercial e cadastral de e-commerce:

- Eliminar tarefas manuais repetitivas na criação de descrições HTML.
- Gerar descrições ricas e padronizadas automaticamente utilizando Inteligência Artificial e pesquisa em tempo real.
- Gerenciar o fluxo de aprovação de produtos (PIM) através de um painel Kanban visual e em tempo real.
- Agilizar a consulta de códigos de **Hierarquia de Grupo de Itens**, **Marcas** e **Categorias** no SAP sem depender do cruzamento manual de planilhas.
- Validar e organizar links de marketplaces de forma rápida.
- Centralizar o acompanhamento analítico e relatórios de desempenho da equipe.
- Oferecer uma experiência de uso fluida, com resposta instantânea e suporte a tema claro/escuro.

---

## 🧰 Ferramentas Integradas

### 1. 🏠 Hub Central (`index.html`)
Painel principal que serve como portal de entrada, permitindo navegar rapidamente entre todas as ferramentas da plataforma.

---

### 2. 🤖 Gerador de Descrições IA (`gerador-descricao-ia.html`)
Motor de criação avançado que utiliza IA para pesquisar e redigir descrições completas baseadas em regras de negócio rigorosas.

- **Pesquisa Inteligente (Tavily API):** Busca automatizada em modo avançado pelas especificações do produto, priorizando o site oficial do fabricante.
- **Geração Restrita (Groq API):** Utiliza LLMs ultrarrápidos com instruções rígidas (anti-alucinação) para não inventar dados e seguir o padrão exato da empresa.
- **Exportação Otimizada:** Gera o código HTML renderizado e permite a exportação automática para Word (`.doc`) com fonte Arial e nomenclatura inteligente (ex: `NAC011068 - Nome do Produto.doc`).
- **Proteção de Tokens:** Lógica interna que corta textos excessivos da web para garantir economia e estabilidade nas requisições da API.

---

### 3. 📝 Formatador de Anúncios (`formatador-anuncios.html`)
Gerador automático de código HTML padronizado estruturalmente.

- **Título Dinâmico:** Formatação inteligente em *Title Case* com preservação de siglas técnicas (ex: `USB`, `HDMI`, `SSD`, `NVME`, `DDR4`, `AM4`).
- **Condição do Produto:** Seleção entre produto *Novo* ou *Recondicionado* (com ajuste automático das regras de garantia e avisos de rodapé).
- **Campos Estruturados:** Separação lógica de Comercial, Especificações, Dimensões, Itens Inclusos, EAN e NAC.

---

### 4. 🔍 Catálogo SAP — Busca de Tabelas (`catalogo-busca-sap.html`)
Buscador unificado local de tabelas estruturais do SAP.

- **Consulta Unificada:** Pesquisa simultânea em **Hierarquia**, **Marca** e **Categoria**.
- **Filtros Avançados:** Filtragem por Nível de Hierarquia (N1 a N6) e ordenação (`A-Z` ou por `ID`).
- **Opções Flexíveis de Cópia e Destaque Visual:** Realce em tempo real e extração automatizada de IDs ou Caminhos.

---

### 5. 🔗 Validador / Buscador de Links (`buscador-links.html`)
Ferramenta para validação, organização e gerenciamento rápido de URLs e links úteis da operação.

---

### 6. 📊 Dashboard de Métricas (`dashboard-metricas.html`)
Painel analítico para acompanhamento de dados operacionais e de e-commerce (KPIs, relatórios e gráficos de produtividade).

---

## ⚡ Destaques Técnicos

- **Arquitetura Front-End + BaaS:** Desenvolvido em HTML5, CSS3 e JavaScript Vanilla.
- **Integrações de API:** Consome as APIs da Groq (LLM) e Tavily (Search) diretamente pelo cliente de forma otimizada.
- **Processamento de Arquivos Locais:** Utiliza a biblioteca `mammoth.js` e a File API nativa do navegador para ler e extrair metadados de arquivos `.docx` arrastados pelo usuário.
- **Privacidade & Armazenamento:** Uso estratégico do `localStorage` para guardar preferências de Tema (Dark/Light Mode) e chaves de API com segurança no navegador do usuário.
- **Design System Responsivo:** Layout limpo, padronizado e otimizado para qualquer resolução de tela.

---

## 📂 Estrutura de Arquivos

```text
Hub-Ferramentas/
├── index.html               # Página principal / Portal do Hub
├── gerador-descricao-ia.html# Motor IA de descrições (Groq + Tavily)
├── PADRÃO-DE-DESCRIÇÃO.txt  # Regras de negócio restritas consumidas pela IA
├── formatador-anuncios.html # Gerador e formatador manual de anúncios HTML
├── catalogo-busca-sap.html  # Buscador de tabelas e hierarquias do SAP
├── buscador-links.html      # Validador e gerenciador de links
├── dashboard-metricas.html  # Dashboard de métricas e KPIs operacionais
└── README.md                # Documentação do repositório
