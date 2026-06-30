---
name: vencefy
description: Use when planejando, criando ou operando conteúdo de LinkedIn ou outbound/social selling do Bento/A360 na ferramenta Vencefy: posts founder, campanhas de conexão/aquecimento/autoridade/relacionamento, cadências, listas de leads, agentes de IA, caixa de entrada e CRM. Cobre os limites de segurança do LinkedIn, a ordem do método (aquecer, conectar, nutrir) e os guardrails de copy do Bento.
argument-hint: "[objetivo: conteúdo | outbound | campanha X | lista de leads]"
allowed-tools: Read, Write, Edit, Glob, Grep
tier: reference
version: 0.1.0
source: "Central de Ajuda Vencefy (33 tutoriais, lida em 2026-06-30) + brain Bento/A360"
---

# gos-vencefy — Operar conteúdo + outbound no Vencefy

## Overview
Vencefy é a plataforma de **outbound + social selling + criação de conteúdo** no LinkedIn (método humanizado, orquestração de agentes de IA). Esta skill traduz os fluxos do Vencefy pro contexto Bento/A360.

**Princípio do método:** value → confiança → conversão. **Aquecer antes de esfriar**; a reunião é consequência, não pressão.

**Segurança:** Vencefy usa API oficial do LinkedIn, comportamento humanizado (intervalos variáveis) e pausa automática se o LinkedIn alertar limite. O maior risco de bloqueio vem de **uso manual simultâneo + outras ferramentas**, não da Vencefy. Não estourar os limites abaixo.

## Contexto Bento (aplicar SEMPRE)
- **ICP Tier 2:** dono/sócio de **empresa de manutenção multi-equipamento** + 2ª geração (filhos 25-40, LinkedIn ativo).
- **Guardrails de copy** (todo texto que sai — post, comentário, nota de conexão, cadência, DM): sem travessão (—); sempre "para", nunca "pra"; **Bento não é ERP** (ERP = vilão); sem "industrial". Detalhe: `memory/shared/decisoes/2026-06-29-copy-guardrails-anti-ai.md`.
- **Prova (mata a probabilidade percebida):** EPM Pontes Rolantes — Roberta Estronioli, sócia-administradora; 442 notas capturadas da SEFAZ sozinho, R$ 3,16 mi conciliados. Founder: 20 anos de engenharia (Walmart).
- Gargalo de venda = **probabilidade percebida** → liderar com prova.

## Mapa do Vencefy

| Módulo | Pra quê |
|---|---|
| Dashboard | Métricas: Geral / Outreach / Social Selling / Conteúdo |
| Campanhas | 5 tipos: Conexão, Aquecimento, Autoridade, Relacionamento, Empresas |
| Conteúdo | Criar + agendar + publicar + medir posts (com agente de IA) |
| Leads | Listas (Pessoas 1º/2º-3º, Empresas), busca no LinkedIn, segmentação |
| Cadências | Réguas de mensagem pós-aceite (param na resposta) |
| Caixa de Entrada | Inbox do LinkedIn sincronizado + tags |
| CRM | Pipeline Kanban (move sozinho em aceite/resposta) |
| Agentes IA | 5 assistentes: Conexão, Caixa de Entrada, Comentários, Respostas, Conteúdo |
| Contas LinkedIn / Equipe / Relatórios / Integrações (N8N) | Infra/gestão |

## A — Criação de Conteúdo (módulo Conteúdo)
Fluxo (Conteúdo → "Novo Projeto"): **conta → URL de inspiração → Agente de IA → Programação (data/hora) → revisar/editar → imagem → "Criar e ativar"**. Abas Calendário (cronograma) e Performance (métricas).

> **REGRA NOSSA (não-negociável):** a copy é **NOSSA**, não auto-gerada genérica. Use o agente de IA como rascunho/assist, mas **reescreve na voz founder + passa os 4 guardrails** antes de ativar. A imagem pode ser gerada aqui dentro (em vez do OpenRouter externo) — ainda assim, sem cara de "AI slop".
> **Por que usar o módulo (e não postar nativo no LinkedIn):** Performance integrada às campanhas + calendário + o conteúdo alimenta o motor de aquecimento.

**7 agentes de conteúdo (formatos):** Lead Magnet (isca), Post Narrativo, História de Autoridade, História de Venda, Conselho de Autoridade, Estudo de Caso, Comentário de Notícia. Escolher por intenção do post (ex: case EPM → Estudo de Caso).

## B — Outbound (sequência do método)
1. **Leads** — construir lista do ICP (ver limites). Fragmentar por estado/cargo/tamanho.
2. **Aquecer** — Campanha de **Aquecimento** nos leads ANTES do convite (curtir posts antigos + comentar via agente em posts originais < 7 dias).
3. **Conectar** — Campanha de **Conexão** (com nota = Agente de Conexão; ou sem nota → cadência direto).
4. **Nutrir** — **Cadência** pós-aceite (intervalo > 0 dias; variáveis Nome/Empresa/Cargo; **para automaticamente quando o lead responde** → assumir manual).
5. **Gerir** — CRM (Kanban move sozinho: aceite → "Convite Aceito", resposta → "Relacionamento"; etapas avançadas manuais) + Caixa de Entrada.

Complementos: **Autoridade** (interagir com Top Voices, ≤25 perfis, 1-4 semanas) · **Relacionamento** (one-shot pra 1º grau — eventos, lançamentos).

## Limites de segurança (NÃO estourar)

| Ação | Limite seguro |
|---|---|
| Convites (Conexão) | 20/dia Premium · 30/dia Sales Navigator |
| Aquecimento (curtidas+comentários) | ~60 interações/dia |
| Relacionamento (DM one-shot) | até 60/dia |
| Autoridade | até 25 perfis |
| Busca de leads | máx **500 leads/busca**, **1000 buscas/dia** |
| Convites pendentes | remover após 30 dias (limpar perfil) |
| Janela de disparo | dias úteis, 08h-20h |
| Cadência | 1º envio com intervalo > 0 dias |

## Agentes de IA (5 tipos)

| Agente | Função | Setup |
|---|---|---|
| Conexão | nota personalizada do convite | IA Magic + escolher estilos de voz |
| Caixa de Entrada | responde chat (Qualificação/Recrutamento/Suporte; BANT, SPIN) | objetivo + FAQ + ferramentas (calendário/PDF) |
| Comentários | comenta em posts de terceiros (aquecimento/autoridade) | IA Magic + estilos |
| Respostas | responde comentários nos SEUS posts | prompt manual + exemplos |
| Conteúdo | gera posts (7 formatos) | IA Magic + formato |

> Preferir **IA Magic** (não manual — evita quebrar regras do LinkedIn). **Treinar com a NOSSA voz** (exemplos reais) e **sempre revisar** o output antes de ativar. Por exigência do LinkedIn, o Agente de Caixa de Entrada se apresenta como assistente virtual.

## Sequência recomendada — teste de 2 semanas (Tier 2)
1. 3 posts founder no módulo Conteúdo (voz nossa) + Agente de Comentários treinado.
2. Campanha de Aquecimento na lista do ICP (interior SP).
3. Campanha de Conexão com nota (Agente de Conexão) + Cadência pós-aceite.
4. Medir: **aceite ≥ 25% (Semana 1)**, **resposta ≥ 15% (Semana 2)**. Se aceite < 25% mesmo trocando público → reconsiderar canal (ver decisão GTM).

## Erros comuns
- Deixar o agente gerar conteúdo genérico e publicar sem reescrever na voz founder (viola posicionamento + guardrails).
- Postar nativo no LinkedIn em vez de pelo módulo Conteúdo (perde Performance integrada).
- Lista de leads ampla demais (> 500) → busca trava em 1000 resultados; fragmentar.
- Disparar convite frio sem aquecer antes.
- Cadência com 0 dias de intervalo (parece robô).
- Esquecer os 4 guardrails de copy.
- Rodar outras ferramentas de automação no mesmo LinkedIn (soma de risco de bloqueio).

## Referências
- Central de Ajuda Vencefy (app.vencefy.com/central-de-ajuda) — 33 tutoriais.
- Brain: `strategy/icp.md`, `memory/shared/decisoes/2026-06-29-copy-guardrails-anti-ai.md`, `sales/epm-case-study.md`, `ofertas/manutencao-multi-equipamento/gtm/`.
