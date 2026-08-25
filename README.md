# 💛 Triagem de Mensagens Instagram — Fique Vivva

Bot de triagem automatizada para o Instagram Direct, construído em n8n 
para o Fique Vivva, projeto de apoio a mulheres em situação de violência 
doméstica.

## 🎯 Problema que Resolve

Mensagens recebidas via Instagram precisavam de triagem manual antes de 
chegarem à pessoa certa da equipe — atrasando o primeiro contato em 
momentos que podem ser sensíveis e urgentes.

## ⚙️ Como Funciona

1. **Recepção da mensagem** — via Webhook da API da Meta (Instagram Direct)
2. **Identificação do contato** — busca se é a primeira mensagem da pessoa
3. **Boas-vindas com menu** — se for o primeiro contato, envia menu com 
   três opções: suporte a vítima de violência, voluntariado, dúvidas
4. **Roteamento por escolha** — direciona a conversa conforme a opção 
   selecionada
5. **Resposta segura** — no fluxo de suporte à violência, a resposta 
   já inclui os canais oficiais de emergência (Central de Atendimento 
   à Mulher — 180, e 190)
6. **Registro estruturado** — cada interação é salva/atualizada em 
   planilha de controle, por tipo de atendimento

## 🛠️ Stack

| Componente | Tecnologia |
|---|---|
| Orquestração | n8n |
| Canal | Instagram Direct (Meta Graph API) |
| Registro de conversas | Google Sheets API |
| Lógica de roteamento | IF / Switch nodes |

## 🔐 Sanitização e Segurança

Esta é uma versão pública sanitizada do fluxo real:
- **Nenhum ID real de planilha está incluído** — a planilha de origem 
  contém registros de pessoas reais e não pode ser exposta
- Tokens de acesso à API da Meta não estão presentes (usam placeholder)
- As mensagens de exemplo neste repositório são simuladas, não 
  conversas reais

## 📂 Estrutura do Fluxo
