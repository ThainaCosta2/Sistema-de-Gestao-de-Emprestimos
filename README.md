# Sistema de Gestão de Empréstimos

### 📝 Visão Geral
Este repositório abriga um projeto criado para a gestão administrativa e financeira de carteiras de empréstimos. O sistema oferece interfaces distintas para **Gerentes** (foco em tomada de decisão e cobrança) e **Clientes** (foco em transparência e acompanhamento de dívidas), garantindo um controle eficiente de fluxo de caixa e inadimplência.
O sistema agora conta com um **Modo Escuro** para melhor conforto visual e uma experiência de usuário aprimorada, além de **gráficos dinâmicos** que oferecem clareza sobre o progresso dos empréstimos e histórico de pagamentos.




https://github.com/user-attachments/assets/aa0ec797-deeb-4d20-9888-0803a587b1ca



https://github.com/user-attachments/assets/f11bba65-fd48-4abe-b3be-0d27728a22ab


### 🎯 Objetivos do Projeto
O objetivo central deste projeto foi desenvolver uma plataforma funcional que automatiza o cálculo de juros e multas por atraso, fornece indicadores visuais de rentabilidade através de gráficos e facilita a comunicação direta com o cliente via integração com WhatsApp, buscando otimizar o processo de recuperação de crédito.
garantindo uma **experiência de usuário intuitiva e visualmente agradável** em ambos os modos de exibição (claro e escuro).

### 🗄️ Bases de Dados
O projeto utiliza um banco de dados relacional para persistência de usuários, cargos e configurações do sistema.
*   **Sincronização Automatizada:** O sistema possui integração total entre a interface web e o banco de dados. Ao cadastrar um novo usuário pelo site, o **ID é gerado automaticamente pelo banco (Auto-increment)** e os dados são persistidos via SQLAlchemy.
*   **DBeaver:** Utilizado como cliente de banco de dados para visualização em tempo real dos registros, estruturação de tabelas e execução de queries de auditoria para validar a integridade dos cálculos financeiros.

### 🚀 Etapas do Projeto
*   **Estruturação Backend:** Desenvolvimento das rotas em Flask e lógica de autenticação baseada em perfis (Gerente/Cliente).
*   **Painel Administrativo:** Criação de dashboards com KPIs de Total Emprestado, Taxa de Atraso e Previsão de Entradas.
*   **Área do Cliente:** Implementação de extratos detalhados, progresso de pagamento em tempo real, **histórico visual de pagamentos com status diferenciados**, simulador de acréscimos e **sistema de alertas flutuantes de inadimplência**.
*   **Módulo de Cobrança:** Integração de API de redirecionamento para WhatsApp com mensagens personalizadas.
*   **Melhorias de UI/UX**: Implementação de **Modo Escuro**, **Sistema de Busca Inteligente** com sugestões de atalhos em tempo real e **validações de formulários** (como a confirmação de senha e campos obrigatórios).
*   **Gestão de Acessos (RBAC):** Controle de permissões baseado em 5 cargos fundamentais: **Administrativo, Desenvolvedor, Financeiro, Gerente e Investidor**.
*   **Lógica de Negócio:** Centralização de cálculos matemáticos de juros, multa e formatação de moeda para garantir consistência em todo o sistema.

### 🛠️ Tecnologias e Bibliotecas

**Linguagens de Programação:**
*   **Python:** Lógica de backend e processamento de dados.
*   **JavaScript:** Interatividade no frontend e renderização de gráficos.
*   **HTML5 & CSS3:** Estrutura e estilização personalizada com variáveis dinâmicas.

**Frameworks e Bibliotecas Backend:**
*   **Flask:** Micro-framework web.
*   **SQLAlchemy:** ORM para manipulação do banco de dados.
*   **Jinja2:** Motor de templates para renderização de HTML dinâmico.

**Frontend e Bibliotecas JS:**
*   **Bootstrap 5:** Framework de design responsivo.
*   **Chart.js:** Biblioteca para geração de gráficos de barras, linhas e roscas.
*   **DataTables:** Manipulação e filtragem avançada de tabelas.
*   **Bootstrap Notify:** Sistema de notificações flutuantes (toasts).
*   **Font Awesome:** Biblioteca de ícones profissionais.

**APIs e Integrações:**
*   **WhatsApp Web API:** Link direto para ações rápidas de cobrança e suporte.

### 🔐 Segurança
O sistema prioriza a proteção dos dados dos usuários:
*   **Sessões Seguras:** Gerenciamento de login via Flask-Session para controle de acesso por perfil.

### 📂 Estrutura do Projeto
```text
├── sistema/
│   ├── models/          # Definição das tabelas e lógica de banco
│   ├── views/           # Rotas e controle das páginas
│   ├── templates/       # Arquivos HTML (Jinja2)
│   └── static/          # CSS, JS e Imagens
├── app.py               # Ponto de entrada da aplicação
├── config.py            # Configurações do banco de dados e chaves
└── mapeamento_roles.py  # Definição dos níveis de acesso
```

### � Conclusão
O projeto entrega uma solução completa de ponta a ponta para o setor financeiro de empréstimos. A separação clara entre a visão administrativa (focada em lucro e saúde do negócio) e a visão do cliente (focada em clareza de dados e facilidade de pagamento) torna a ferramenta robusta e escalável para cenários reais de mercado.
A inclusão do **Modo Escuro** e a **melhoria na visualização dos dados gráficos** reforçam o compromisso com a usabilidade e a clareza, tornando a ferramenta ainda mais robusta e escalável para cenários reais de mercado.
