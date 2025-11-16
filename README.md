

# 🧠 Descrição do Projeto

O **Smart_FUP-AI** é um agente de automação inteligente capaz de transformar **transcrições de reuniões comerciais** em **planos de ação objetivos**, incluindo follow-up, tarefas e próximos passos.

Combinando **Azure OpenAI**, **Foundry** e **Logic Apps**, o agente interpreta o conteúdo da conversa e produz resultados estruturados e acionáveis para times comerciais.

---

## 🎯 Objetivo do Agente

Automatizar o pós-reunião comercial, garantindo clareza, rapidez e organização no follow-up.
    📌 Reduz o esforço manual dos times de vendas e atendimento

    📌 Padroniza a comunicação com clientes, evitando esquecimentos ou inconsistências

    📌 Gera insights estratégicos a partir das transcrições, identificando oportunidades de negócio

    📌 Transforma decisões em ações concretas, com tarefas e próximos passos bem definidos

    📌 Acelera o ciclo comercial, aumentando a eficiência e a taxa de conversão

## Exemplo

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
|**Azure CLI + SDK** |	Autenticação e execução local do agente |


---
## ▶️ Execução Local

### 1. Preparar ambiente virtual
```bash
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
2. Configurar variáveis no .env
env
AZURE_AI_ENDPOINT=https://<nome-do-recurso>.cognitiveservices.azure.com/
AGENT_NAME=<Agent ID do Foundry>
3. Autenticar no Azure
bash
brew install azure-cli   # se não tiver instalado
az login
az account show          # confirmar assinatura ativa
4. Rodar o agente
bash
python main.py
5. Exemplo de mensagem
python
message = project.agents.messages.create(
    thread_id=thread.id,
    role="user",
    content="Resumo da reunião: Cliente pediu proposta até terça-feira, mencionou interesse em desconto e quer agendar demo. Gere um follow-up."
)
Instalação de Dependências Coloque o requirements.txt também em bloco de código:
txt
azure-ai-projects==1.0.0b2
azure-ai-agents==1.0.0b2
azure-identity==1.17.1
python-dotenv==1.0.1 
```
---

## 📁 Estrutura do Projeto

README.md             → Documentação principal do projeto
src/
  ├── agent.json      → Definição do agente em formato OpenAPI
  └── instruction-agent.txt → Exemplo das instruções do agente
foundry-config.md     → Guia de execução e diagrama de configuração no Foundry
examples/
  ├── entrada-transcricao.txt → Transcrição bruta da reunião
  ├── saida-relatorio.json    → Saída estruturada gerada pelo agente
  └── email-html-gerado.html  → E-mail de follow-up em HTML
main.py               → Script principal para rodar o agente via SDK
.env.example          → Exemplo de configuração de variáveis de ambiente
img/agent/            → Prints da configuração do agente
img/input/            → Print do prompt do usuário
img/output/           → Resultados gerados pelo agente
img/test/             → Prints de testes e validações
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