

## 🧠 Descrição do Projeto

O **Smart_FUP-AI** é um agente de automação inteligente capaz de transformar **transcrições de reuniões comerciais** em **planos de ação objetivos**, incluindo follow-up, tarefas e próximos passos.

Combinando **Azure OpenAI**, **Foundry** e **Logic Apps**, o agente interpreta o conteúdo da conversa e produz resultados estruturados e acionáveis para times comerciais.

---

## 🎯 Objetivo do Agente

Automatizar o pós-reunião comercial, garantindo clareza, rapidez e organização no follow-up.

# Exemplo

**Entrada:**  
Transcrição de uma reunião comercial.

**Saída:**  
- Resumo estratégico  
- Pontos-chave discutidos  
- Estratégias de follow-up  
- Sugestão de e-mail  
- Lista de tarefas e próximos passos  

---

## ⚙️ Funcionalidades Principais

- ✅ Processamento da transcrição de reuniões  
- ✅ Análise semântica com Azure OpenAI  
- ✅ Geração automática de plano de ação  
- ✅ Sugestão de follow-up comercial e e-mail  
- ✅ Integração com Logic Apps  
- ✅ Agente executável diretamente no Foundry  

---

## 🧩 Tecnologias Utilizadas

| Tecnologia | Utilização |
|-----------|------------|
| **Azure OpenAI** | Modelo GPT-4o-mini para análise e geração de ações |
| **Foundry (Microsoft)** | Execução, prompt, interface do agente |
| **Logic Apps** | Envio automático de e-mail e automações |
| **GitHub** | Repositório do código e documentação |


---

## 📁 Estrutura do Projeto

| Pasta/Arquivo        | Descrição                                                                 |
|-----------------------|---------------------------------------------------------------------------|
| README.md             | Documentação principal do projeto                                         |
| agent.json            | Definição do agente em formato OpenAPI                                    |
| foundry-config.md     | Guia de execução e configuração no Foundry                                |
| examples/             | Exemplos reais de entrada e saída                                         |
| ├── entrada-transcricao.txt | Transcrição bruta da reunião                                        |
| ├── saida-relatorio.json    | Saída estruturada gerada pelo agente                                |
| └── email-html-gerado.html  | E-mail de follow-up em HTML                                         |
| img/agent/            | Prints da configuração do agente                             |
| img/output/           | Resultados gerados pelo agente                                           |
| img/test/             | Prints de testes e validações  

## 🔗 Referências

Azure OpenAI → https://learn.microsoft.com/en-us/azure/ai-services/openai/
Foundry → https://foundry.microsoft.com/
Power Automate → https://learn.microsoft.com/en-us/power-automate/
GitHub Guides → https://guides.github.com/
Microsoft Learn for Students → https://learn.microsoft.com/en-us/users/student-hub/

## 👩‍💻 Autoria

Desenvolvido por Franciele Borges
Projeto criado para o desafio Azure Frontier Girls com foco em automação inteligente usando Foundry + Azure AI + Logic Apps.