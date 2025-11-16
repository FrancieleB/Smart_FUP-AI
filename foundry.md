# 🚀 Como Criar e Executar o Agente

Abaixo está o passo a passo completo, com as imagens do projeto.

## 1️⃣ Criar o Recurso Azure OpenAI

- Acesse o **Azure Portal**  
- Crie o recurso **Azure OpenAI**  
- Defina nome, grupo de recursos e região permitida  

📷 *Imagem:*  
![resource-group](img/agent/resource-group.png)

---

## 2️⃣ Deploy do Modelo (GPT-4o-mini)

- Abra o recurso Azure OpenAI  
- Vá em **Deployments**  
- Faça o deploy do modelo **gpt-4o-mini**  

📷 *Imagem:*  
![deploy-model](img/agent/deploy-agent.png)

---

## 3️⃣ Criar o Agente no Foundry

- Acesse o Foundry  
- Clique em **Create Agent**  
- Configure:
  - Nome: Smart_FUP-AI  
  - Descrição  
  - Objetivo  
  - Chave/API do Azure OpenAI  

📷 *Imagem:*  
![foundry-agent-create](img/agent/config-agent.png)

---

## 4️⃣ Configurar o Prompt Principal

O prompt define o comportamento do agente:

- Interpreta a transcrição  
- Extrai tópicos essenciais  
- Gera follow-up  
- Estrutura tarefas  
- Sugere e-mail automático  

📷 *Imagem:*  
![prompt-config](img/agent/definicao-fluxo.png)

---

## 5️⃣ Criar Automação no Logic Apps

Aqui criamos o fluxo responsável por:

- Receber a saída do agente  
- Disparar:
  - E-mail de follow-up  
  - Criação de tarefas (opcional)

📷 *Imagem:*  
![logicapps-flow](img/agent/config-Logic-app4.png)

---

## 6️⃣ Testar o Agente

Após inserir uma transcrição real ou simulada, validamos:

- Resumo  
- Pontos principais  
- Follow-up  
- Tarefas  
- Corpo do e-mail sugerido  

📷 *Exemplos de entrada:*  
![agent-input1](img/input/entrada1.png)

📷 **Exemplos de saída:* 
1. 
![agent-output1](img/output/resultado1.png) 
2.   
![agent-output2](img/test/teste2.png)

---

## 🔄 Fluxo da Solução
```mermaid
flowchart TD
    A[Transcrição da Reunião] --> B[Foundry Agent]
    B --> C[Azure OpenAI - gpt-4o-mini]
    C --> D[Saída Estruturada: resumo, follow-up, tarefas]
    D --> E[Power Automate / Logic Apps]
    E --> F[Envio de E-mail / Criação de Tarefas]
```

## 📊 Estrutura de Output Produzido

O agente organiza o resultado nos seguintes blocos:

1. Resumo da Reunião
    Contexto e síntese geral.

2. Pontos-Chave
    Tópicos discutidos e decisões.

3. Oportunidades
    Dores, necessidades e possibilidades de negócio.

4. Follow-Up Estratégico
    Passos recomendados com base na conversa.

5. Sugestão de E-mail
    Texto automático para envio ao cliente.

6. Tarefas
    Lista objetiva do que precisa ser feito.

📁 Exemplos → [examples/](./examples/)

## ✅ Conclusão

Com este fluxo configurado, o agente **Smart_FUP-AI** está pronto para transformar transcrições de reuniões comerciais em relatórios estruturados e e-mails de follow-up automáticos.  
A documentação acima garante que qualquer pessoa consiga replicar o processo no **Azure OpenAI + Foundry + Logic Apps**.
