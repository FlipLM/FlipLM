# Case 04 — CPRE Studio (Plataforma de Estudos IREB CPRE-FL com IA & RAG)

**Domínio:** EdTech / Certificação em Engenharia de Requisitos (IREB CPRE Foundation Level)  
**Repositório:** Público ([`FlipLM/ireb-cpre-studio`](https://github.com/FlipLM/ireb-cpre-studio))  
**Demonstração:** https://ireb-cpre-studio.vercel.app  
**Stack:** `Next.js 15` · `React 19` · `TypeScript` · `Tailwind CSS 4` · `Supabase (PostgreSQL + Auth + RLS + FTS)` · `Vercel` · `PWA` · `Vitest`

[← Voltar ao Portfólio Principal](../README.md)

---

## 1. O Problema

A preparação para a certificação **IREB CPRE Foundation Level** exige domínio preciso de terminologia oficial (Syllabus v3.x), prática constante com questões de resposta única e múltipla, revisão espaçada de erros recorrentes e explicações conceituais sem receber "spoilers" imediatos do gabarito. Além disso, o estudo precisa acontecer tanto no desktop quanto no celular (PWA instalável), sem custo de infraestrutura paga.

---

## 2. A Solução

O **CPRE Studio** foi construído como uma plataforma Full Stack completa de estudos, simulados e tutoria assistida por IA:

- **Banco de 225 Questões IREB CPRE-FL:** 169 questões de resposta única e 56 de múltipla resposta (exigindo correspondência exata do conjunto), incluindo 11 questões com diagramas/figuras, explicações detalhadas e taxonomia nas 7 áreas temáticas da certificação.
- **Modo Estudo, Simulados Cronometrados & Revisão Espaçada (SM-2):** simulação real com gabarito bloqueado durante a prova, fila de revisão de erros por streak de acertos, favoritos, anotações pessoais, dashboard analítico e gráficos de evolução por tópico.
- **Prof. IREB — Tutor Interativo em Pixel Art (Visual Novel):**
  - Sprites autorais 64×64/512px com 5 animações (`idle`, `talking`, `thinking`, `angry_slam`, `celebrate_clap`), tamanho configurável (`P / M / G / GG`) no desktop e **popup flutuante transparente, arrastável e redimensionável** com menu lateral de chat no mobile.
  - **Skill Pedagógica Parametrizável (`prompts/professor-ireb.skill.md`):** carrega diretrizes em tempo real separando **Pedir Dica** (pontos-chave progressivos sem entregar a resposta) e **Perguntar** (Modo Aula Liberal para aprender a teoria antes de responder).
- **Base de Conhecimento Oficial (RAG) no Supabase:** tabela `ireb_knowledge_base` com **Full-Text Search em Português (`tsvector` + índice `GIN`)** contendo as **7 Unidades Educacionais (EU 1 a EU 7)** do Syllabus oficial IREB CPRE-FL (incluindo os 9 Princípios Fundamentais). Toda dica ou dúvida consulta primeiro essa base e exibe na UI quais unidades oficiais embasaram a resposta.
- **Cascata Multi-IA 100% Gratuita com Fallback Automático:** orquestração server-side em cascata (`Groq` → `Cerebras` → `OpenRouter :free` com trava anti-modelos-pagos → `Gemini`), garantindo alta disponibilidade e respostas em sub-segundo sem custo fixo.
- **Autenticação, Isolamento RLS, Keep-Alive e PWA:** login/cadastro via Supabase Auth com **Row Level Security (`auth.uid() = user_id`)** em 10 tabelas, cron na Vercel (`0 9 */3 * *` em `/api/keepalive`) para manter o Supabase gratuito sempre ativo e Service Worker (`sw.js`) + Web App Manifest para instalação nativa no celular.

---

## 3. Capturas de Tela (Ambiente em Produção)

### Modo Estudo com Prof. IREB (Tutor Interativo em Pixel Art + RAG)
![CPRE Studio — Modo Estudo com Prof. IREB](../assets/ireb-estudar.png)

### Visão Geral (Dashboard Real e Recomendações Priorizadas)
![CPRE Studio — Visão Geral](../assets/ireb-dashboard.png)

### Configurador de Simulados Cronometrados
![CPRE Studio — Simulados](../assets/ireb-simulados.png)

### Relatórios e Mapa de Domínio por Assunto
![CPRE Studio — Relatórios e Mapa de Domínio](../assets/ireb-relatorios.png)

---

## 4. Evidências de Engenharia

- **Integridade testada com Vitest:** suíte automatizada validando as 225 questões, gabaritos únicos e múltiplos, ausência de duplicidades, resolução de imagens e bloqueio de gabarito durante simulados em andamento.
- **Arquitetura resiliente Custo Zero:** hospedagem serverless na Vercel + PostgreSQL/Auth no Supabase + Keep-Alive automático + fallback multi-provedor de IA.

---

[← Voltar ao Portfólio Principal](../README.md)
