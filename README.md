# 🛠️ Hub de Ferramentas Operacionais

Uma suíte web leve, ágil e centralizada para otimização de processos de e-commerce, cadastro de produtos no ERP SAP, formatação padronizada de anúncios e acompanhamento de métricas.

🚀 **Acesse o projeto online:** [https://dgmarques-br.github.io/Hub-Ferramentas/](https://dgmarques-br.github.io/Hub-Ferramentas/)

---

## 📌 Sobre o Projeto

O **Hub de Ferramentas Operacionais** foi desenvolvido para resolver problemas recorrentes da rotina comercial e cadastral de e-commerce:

* Eliminar tarefas manuais repetitivas na criação de descrições HTML.
* Agilizar a consulta de códigos de **Hierarquia de Grupo de Itens**, **Marcas** e **Categorias** no SAP sem depender do cruzamento manual de planilhas.
* Validar e organizar links de marketplaces de forma rápida.
* Centralizar o acompanhamento analítico e relatórios de desempenho da equipe.
* Oferecer uma experiência de uso fluida, com resposta instantânea e suporte a tema claro/escuro.

---

## 🧰 Ferramentas Integradas

### 1. 🏠 Hub Central (`index.html`)
Painel principal que serve como portal de entrada, permitindo navegar rapidamente entre todas as ferramentas da plataforma.

---

### 2. 📝 Formatador de Anúncios (`formatador-anuncios.html`)
Gerador automático de código HTML padronizado para plataformas ERP e marketplaces.

* **Título Dinâmico:** Formatação inteligente em *Title Case* com preservação de siglas técnicas (ex: `USB`, `HDMI`, `SSD`, `NVME`, `DDR4`, `AM4`).
* **Condição do Produto:** Seleção entre produto *Novo* ou *Recondicionado* (com ajuste automático das regras de garantia e avisos de rodapé).
* **Campos Estruturados:**
  * **Descrição Comercial** e **Especificações Técnicas** separadas (com aplicação automática de negrito no formato `Chave: Valor`).
  * **Dimensões e Peso:** Inserção automática das unidades de medida (`cm` e `kg`).
  * **Itens Inclusos:** Limpeza automática de marcadores indesejados (`-`, `*`, `•`).
  * **Identificação:** Suporte a código **NAC** (em negrito completo) e código **EAN**.
* **Visualização Real e Código HTML:** Alternância rápida entre o código-fonte HTML e o resultado renderizado, com botões para copiar com um único clique.

---

### 3. 🔍 Catálogo SAP — Busca de Tabelas (`catalogo-busca-sap.html`)
Buscador unificado local de tabelas estruturais do SAP.

* **Consulta Unificada:** Pesquisa simultânea por nome ou ID em **Hierarquia de Grupo de Item**, **Marca** e **Categoria**.
* **Filtros Avançados:** Filtragem por Nível de Hierarquia (N1 a N6) e ordenação (`A-Z` ou por `ID`).
* **Opções Flexíveis de Cópia:**
  * Modo **ID**: Copia o código numérico do registro ao clicar na linha.
  * Modo **Caminho**: Copia automaticamente apenas a categoria/termo final da árvore hierárquica (ex: copia apenas `FERRAMENTAS PARA BATERIA`).
* **Destaque Visual (*Highlight*):** Realce dos termos pesquisados na tabela em tempo real.

---

### 4. 🔗 Validador / Buscador de Links (`buscador-links.html`)
Ferramenta para validação, organização e gerenciamento rápido de URLs e links úteis da operação.

---

### 5. 📊 Dashboard de Métricas (`dashboard-metricas.html`)
Painel analítico para acompanhamento de dados operacionais e de e-commerce.

* **Visualização de KPIs:** Monitoramento de métricas essenciais de desempenho da equipe e volume de cadastros.
* **Relatórios e Gráficos:** Acompanhamento visual de progresso e produtividade operacional.

---

## ⚡ Destaques Técnicos

* **100% Client-Side:** Desenvolvido em HTML5, CSS3 e JavaScript Vanilla. Não requer servidor backend, banco de dados ou instalação de dependências.
* **Privacidade & Segurança:** Os dados não são enviados para nenhum servidor externo; todo o processamento ocorre localmente no navegador do usuário.
* **Modo Escuro / Claro (Dark Mode):** Alternância de temas com salvamento automático das preferências no `localStorage`.
* **Design System Responsivo:** Layout limpo e otimizado para qualquer resolução de tela.

---

## 📂 Estrutura de Arquivos

```text
Hub-Ferramentas/
├── index.html               # Página principal / Portal do Hub
├── formatador-anuncios.html # Gerador e formatador de anúncios em HTML
├── catalogo-busca-sap.html  # Buscador de tabelas e hierarquias do SAP
├── buscador-links.html      # Validador e gerenciador de links
├── dashboard-metricas.html  # Dashboard de métricas e KPIs operacionais
└── README.md                # Documentação do repositório
