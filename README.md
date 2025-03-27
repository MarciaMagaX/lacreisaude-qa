# lacreisaude-qa
"Projeto de testes para a Lacrei Saúde".
📌 Projeto de Testes - LaCreisaúde Paciente

🔗 Ambiente de Testes: LaCreisaúde Staging

📋 Sumário

⚙️ Pré-requisitos

🚀 Configuração Inicial

🔍 Execução de Testes Manuais

🤖 Execução de Testes Automatizados (Cypress)

⚡ Testes de Desempenho (k6)

♿ Testes de Acessibilidade (Lighthouse/Axe)

📱 Testes de Responsividade

🐞 Registro de Bugs

🔄 Integração Contínua (CI/CD)

📂 Estrutura do Projeto

✅ Próximos Passos

⚙️ Pré-requisitos

Antes de começar, instale:

✅ Node.js (v16 ou superior) → Download Node.js

✅ Git → Download Git

✅ Visual Studio Code (ou outra IDE) → Download VSCode

✅ Google Chrome ou Firefox (para testes manuais e automatizados)

✅ Cypress (será instalado via npm)

✅ k6 (para testes de desempenho) → Instalação k6

🚀 Configuração Inicial

Clone o repositório:

git clone https://github.com/seu-usuario/lacreisaude-qa-project.git
cd lacreisaude-qa-project

Instale as dependências:

npm install

Configure as variáveis de ambiente: Crie um arquivo .env na raiz do projeto com:

BASE_URL=https://paciente-staging.lacreisaude.com.br
TEST_EMAIL=teste@exemplo.com
TEST_PASSWORD=SenhaSegura@123

🔍 Execução de Testes Manuais

📄 Casos de Teste em Gherkin: Localizados em /docs/test-cases/ (ex: cadastro.feature).

🎥 Grave a execução: Use OBS Studio ou Loom e salve os vídeos em /recordings/.

🤖 Execução de Testes Automatizados (Cypress)

Modo interativo:

npx cypress open

Selecione o navegador (Chrome/Firefox).

Escolha o teste a ser executado (ex: registration.cy.js).

Modo headless:

npx cypress run --browser chrome

Gerar relatório HTML (opcional):

npx cypress run --reporter mochawesome

Relatório salvo em /cypress/reports/.

⚡ Testes de Desempenho (k6)

Instale o k6:

# Linux/Mac:
brew install k6

# Windows (Chocolatey):
choco install k6

Execute o teste de carga:

k6 run docs/performance/search-profissional-test.js

Métricas coletadas:

⏳ Tempo de resposta

❌ Taxa de erro

📊 Requisições por segundo

♿ Testes de Acessibilidade

Via Lighthouse (Chrome DevTools):

Abra o site → Pressione F12 → Acesse Lighthouse → Selecione Accessibility.

Via Axe (Cypress):

npx cypress run --spec "cypress/e2e/accessibility.cy.js"

📱 Testes de Responsividade

Via Chrome DevTools:

Ctrl+Shift+M ou F12 → Toggle Device Toolbar.

Via Cypress:

npx cypress run --spec "cypress/e2e/responsiveness.cy.js"

🐞 Registro de Bugs

Modelo de relatoório:

**Título**: [BUG] Botão de cadastro não valida email corretamente

**Descrição**:  
Ao inserir um email sem "@", o sistema permite o cadastro.

**Passos para reproduzir**:  
1. Acesse `/cadastro`.
2. Preencha todos os campos, mas use "emailinvalido".
3. Clique em "Cadastrar".

**Comportamento esperado**: Erro: "Email inválido".
**Comportamento atual**: Cadastro é realizado.
**Severidade**: Alta  
**Prioridade**: Alta  
**Plataforma**: Chrome Mobile  

🔄 Integração Contínua (CI/CD)

✅ GitHub Actions:

Arquivo .github/workflows/tests.yml configurado para rodar testes a cada push ou pull request.

📊 Verifique os resultados:

Acesse Actions no GitHub → Veja os logs de execução.

📂 Estrutura do Projeto

**lacreisaude-qa-project/**

├── .github/               # Configurações CI/CD

├── cypress/               # Testes automatizados

├── docs/                  # Casos de teste (Gherkin)

├── recordings/            # Vídeos de testes manuais

├── bug-reports/           # Relatórios de bugs

├── .env                   # Variáveis de ambiente

└── README.md              # Este guia

✅ Próximos Passos

✔ Execute testes manuais seguindo /docs/test-cases/. ✔ Automatize fluxos críticos com Cypress. ✔ Monitore desempenho com k6. ✔ Reporte bugs encontrados.
