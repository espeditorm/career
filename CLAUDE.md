# Projeto: candidaturas de Espedito Roza (Dito)

Objetivo: encontrar vagas e deixar **pacotes de candidatura prontos** para o Espedito só anexar os
arquivos e enviar. O Claude **não envia** candidaturas (exige login/ação dele); ele prepara tudo.

## Perfil e critérios
- Fonte do perfil: `00_BASE/curriculo/*.pdf` e `00_BASE/respostas_padrao.md` (não inventar fatos,
  métricas ou histórias que não estejam lá).
- Cargos: Senior Product Designer, Senior UX Designer, Senior UI Designer (e UX/UI sênior).
- Local: remoto para empresa de fora aceitando Brasil/LATAM, **ou** São Paulo (remoto/híbrido/presencial).
- Salário mínimo: **US$ 4.000/mês** (≈ R$ 20.400 com US$1 = R$5,10). Descartar vagas abaixo e registrar em `03_DESCARTADAS.md` com o motivo.
- Pontos fortes para destacar: banking/fintech (Open Finance, PIX, crédito, credit unions EUA),
  healthtech (triagem em 150+ hospitais), gov/segurança pública, design system, BA/especificação,
  liderança (tribe lead, 10 squads), ensino de UX/UI, inglês fluente.

## Estrutura
- `README.md`: painel com todas as vagas prontas, prioridade, arquivos a anexar e status (checkbox).
- `00_BASE/`: currículos EN/PT (PDF + DOCX) e banco de respostas.
- `01_VAGAS/NN_Empresa_Cargo/README.md`: um por vaga, contendo:
  1. Link direto de candidatura, plataforma (Greenhouse/Lever/Ashby/Workable/Gupy), data validada.
  2. Resumo da vaga (2–3 linhas), por que combina, salário publicado ou estimado.
  3. **Arquivos para anexar** (caminho exato do currículo e, se houver, da carta).
  4. **Passo a passo do formulário, TODAS as etapas/páginas**, cada campo com a resposta pronta
     para copiar (incluindo perguntas customizadas, dropdowns e sim/não). Gupy e Workable têm várias
     etapas; Gupy costuma ter testes/perguntas depois do cadastro: listar todas.
  5. `cover_letter.txt` quando o formulário tiver campo de carta (texto humano, específico da empresa, ≤ 250 palavras).
- `02_LEADS_A_VALIDAR.md`: vagas encontradas ainda não validadas.
- `03_DESCARTADAS.md`: vagas avaliadas e descartadas com motivo.

## Como validar formulários (precisa de rede liberada)
- Greenhouse: `https://boards-api.greenhouse.io/v1/boards/{board}/jobs/{id}?questions=true` (todas as perguntas, incl. EEO e compliance).
- Lever: HTML de `https://jobs.lever.co/{empresa}/{id}/apply` (cards customizados ficam em `cards[...]`/`customQuestions`).
- Ashby: `POST https://jobs.ashbyhq.com/api/non-user-graphql?op=ApiJobPosting` (`applicationForm` + `surveyForms`); compensação em `api.ashbyhq.com/posting-api/job-board/{org}?includeCompensation=true`.
- Workable: `https://apply.workable.com/api/v1/accounts/{conta}/jobs/{shortcode}/form`.
- Gupy: página da vaga + etapas. Se não der para ver as etapas pós-cadastro, avisar no README da vaga.
- Se a vaga estiver fechada (404/"no longer accepting"), mover para `03_DESCARTADAS.md`.

## Estilo dos textos
Humano, direto, específico da empresa, sem clichês ("passionate", "synergy") e sem travessões em excesso.
Inglês para vagas internacionais, português para vagas brasileiras que estejam em português.
