# lacreisaude-qa
🔍 Plano de Testes – LaCrei Saúde (Mobile e Desktop)

📋 Sumário

1️⃣ Configuração do Ambiente

2️⃣ Execução de Testes Manuais

3️⃣ Execução de Testes Automatizados (Cypress + Cucumber)

4️⃣ Testes de Desempenho (k6)

5️⃣ Testes de Acessibilidade (Lighthouse + Axe)

6️⃣ Testes de Responsividade (Mobile e Desktop)

7️⃣ Registro e Gerenciamento de Bugs

8️⃣ Integração Contínua (CI/CD)

9️⃣ Estrutura do Projeto

🔟 Próximos Passos



1️⃣ Configuração do Ambiente

🛠️ Pré-requisitos

✅ Node.js (v16 ou superior)

✅ Git

✅ Visual Studio Code (ou outra IDE)

✅ Google Chrome ou Firefox

✅ Cypress e Cucumber

✅ k6 (para testes de desempenho)


🚀 Configuração Inicial
Clone o repositório:

git clone https://github.com/seu-usuario/lacreisaude-qa-project.git
cd lacreisaude-qa-project
Instale as dependências:

npm install
Crie um arquivo .env com:

BASE_URL=https://paciente-staging.lacreisaude.com.br  
TEST_EMAIL=teste@exemplo.com  
TEST_PASSWORD=SenhaSegura@123  

2️⃣ Execução de Testes Manuais

📄 Casos de Teste (Gherkin) armazenados em /docs/test-cases/.

📝 Fluxos principais a testar (Mobile)

✅ Cadastro da pessoa usuária: Cadastro → Pós Cadastro → Buscar Profissional

✅ Busca de profissional de saúde: Buscar Profissional → Contatar Profissional

✅ Edição de perfil: Atualizar informações e validar mudanças

✅ Recuperação de senha: Validar fluxo via e-mail

🎥 Gravação dos Testes

📌 Usar OBS Studio ou Loom

📂 Armazenar gravações em /recordings/

📌 Critérios de Aceite

✔ Casos de teste documentados no GitHub

✔ Testes funcionais sem interrupções críticas

✔ Gravações armazenadas


3️⃣ Execução de Testes Automatizados (Cypress + Cucumber)

📍 Rodando testes interativos:

npx cypress open  
📍 Rodando testes em modo headless:

npx cypress run --browser chrome  
📍 Executando testes Cucumber:

npx cypress run --spec "cypress/e2e/*.feature"  
📍 Gerando relatório HTML:

npx cypress run --reporter mochawesome  
📂 Relatório salvo em /cypress/reports/

📌 Critérios de Aceite

✔ Testes automatizados documentados

✔ Testes rodando no pipeline de CI

✔ Relatórios gerados e arquivados


4️⃣ Testes de Desempenho (k6)

📍 Executar teste de carga:

k6 run docs/performance/search-profissional-test.js 

📍 Coletar métricas:

✅ Tempo de resposta

✅ Estabilidade sob carga

✅ Requisições por segundo


📂 Relatórios documentados e armazenados no GitHub

📌 Critérios de Aceite

✔ Relatório documentado no README

✔ Gargalos identificados e relatados


5️⃣ Testes de Acessibilidade (Lighthouse + Axe)

📍 Lighthouse (Chrome DevTools)

Pressione F12 → Acesse Lighthouse

Selecione Accessibility e gere o relatório

📍 Axe via Cypress:

npx cypress run --spec "cypress/e2e/accessibility.cy.js" 

📂 Resultados armazenados no GitHub

📌 Critérios de Aceite

✔ Conformidade com WCAG 2.1

✔ Documentação com insights e melhorias


6️⃣ Testes de Responsividade

📍 Chrome DevTools:

Pressione F12 → Ctrl+Shift+M

Teste em resoluções mobile e desktop

📍 Automação com Cypress:

npx cypress run --spec "cypress/e2e/responsiveness.cy.js"  

📂 Relatórios armazenados no GitHub

📌 Critérios de Aceite

✔ Responsividade validada

✔ Relatórios no README


7️⃣ Registro e Gerenciamento de Bugs

📍 Modelo de relato:

### [BUG] Erro na validação de e-mail  

**Descrição:**  
Ao inserir um e-mail sem "@", o cadastro é realizado.  

**Passos para reproduzir:**  
1. Acesse `/cadastro`  
2. Insira "emailinvalido"  
3. Clique em "Cadastrar"  

**Comportamento esperado:**  
- Mensagem de erro "E-mail inválido"  

**Comportamento atual:**  
- Cadastro é realizado  

**Severidade:** Alta  
**Prioridade:** Alta  
**Evidências:** (Prints e vídeos) 

📂 Bugs armazenados em /bug-reports/

📌 Critérios de Aceite

✔ Relatórios claros e completos

✔ Melhorias propostas


8️⃣ Integração Contínua (CI/CD)

📍 Configuração do GitHub Actions

Arquivo .github/workflows/tests.yml executa:

✅ Testes automatizados

✅ Testes de acessibilidade

✅ Testes de desempenho

📂 Logs disponíveis em "Actions" no GitHub

📌 Critérios de Aceite

✔ Testes rodando a cada commit

✔ Relatórios salvos automaticamente


9️⃣ Estrutura do Projeto
**lacreisaude-qa-project/**

├── .github/            # Configuração do CI/CD

├── cypress/            # Testes automatizados

├── docs/               # Casos de teste (Gherkin)

├── recordings/         # Vídeos dos testes

├── bug-reports/        # Relatórios de bugs

├── .env                # Variáveis de ambiente

└── README.md           # Guia completo do projeto

🔟 Próximos Passos

✔ Executar casos de teste manuais

✔ Automatizar fluxos críticos com Cypress + Cucumber

✔ Monitorar desempenho e acessibilidade

✔ Documentar melhorias


