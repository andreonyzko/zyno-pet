# Documentação do Projeto Zyno

## 1. Introdução

Esta documentação descreve o projeto **Zyno (Pet de Mesa)** — um assistente virtual interativo com rosto animado capaz de interpretar comandos de voz, integrar-se a dispositivos inteligentes e responder por IA.

## 2. Visão Geral do Sistema

O Zyno é dividido em um frontend baseado em web (GitHub Pages) e um backend proxy minimalista (Node.js via Render). O sistema foi projetado para ser seguro, modular, customizável e fácil de implantar.

## 3. Escopo e Objetivos

- Fornecer um assistente virtual que responde ao nome personalizável.
- Suporte a comandos de voz para automação (smart home), mídia, perguntas gerais e configurações.
- Integração com APIs externas via backend proxy (Perplexity, Tuya, YouTube, etc.).
- Oferecer uma experiência visual agradável e interativa.

## 4. Componentes Principais

- **Frontend**: Interface animada em HTML5/CSS/JavaScript, rodando estática no GitHub Pages.
- **Backend Proxy**: Serviço Node.js/Express hospedado em Render, repassando chamadas para APIs externas.
- **APIs Externas**: Integrações com Perplexity (IA), Tuya (smart home), Google Calendar, YouTube, entre outros.
- **LocalStorage**: Configurações, nome do assistente e chaves de API são persistidos localmente.

## 5. Requisitos Funcionais

- O pet animado deve responder à palavra de ativação (default: “Zyno”).
- O sistema deve aceitar comandos de voz e interpretar intenções (NLP local).
- O usuário pode customizar nome do pet e chaves via UI.
- Dispositivos inteligentes podem ser controlados por comandos de voz.
- Perguntas abertas são respondidas via API de IA.
- Todas as ações devem ser refletidas visualmente (animações do rosto).

## 6. Requisitos Não Funcionais

- **Segurança**: Chaves de API jamais ficam armazenadas no backend.
- **Privacidade**: Wake word processada localmente. Reconhecimento de fala enviado somente após ativação.
- **Desempenho**: Baixa latência perceptível nas respostas.
- **Responsividade**: Interface adaptada a diferentes resoluções.

## 7. Tecnologias Utilizadas

| Camada | Tecnologias |
| --- | --- |
| Front-end | HTML5, CSS3, JavaScript, Porcupine Web, NLP.js |
| Backend Proxy | Node.JS |
| APIs | Perplexity, Tuya, Google Calendar |
| Deploy | Github Pages, Render |
| Persistência | localStorage |

## 8. Diagrama de Fluxo Principal

 Exibe animação idle.
- Detecta palavra de ativação.
- Ativa reconhecimento de voz.
- Processa intenção com NLP.js.
- Executa ação local ou repassa via backend.
- Mostra resultado/feedback (expressão, fala ou ação).
- Retorna ao estado idle/escuta.

## 9. Padrões e Convenções

- Todas as respostas de APIs externas chegam ao frontend via proxy.
- Configurações persistentes apenas no browser.
- Nomenclatura clara para intents/actions no NLP.
- Códigos de status RESTful nas respostas backend.

## 10. Considerações Finais

O Zyno é um projeto modular, expansível e facilmente adaptável. Futuras melhorias previstas incluem múltiplos idiomas, histórico de comandos, mais integrações de serviços e personalização visual de alto nível.
