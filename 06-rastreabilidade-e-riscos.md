# 06 · Rastreabilidade e riscos

## Matriz de rastreabilidade

| Problema | Requisito | Regra | História | Teste de aceite |
|:--------:|:---------:|:-----:|:--------:|-----------------|
| P1 | RF-02, RF-03, RF-08 | RN-01, RN-03, RN-04 | HU-01, HU-04 | Conflito de horário recusado |
| P2 | RF-05, RF-06 | RN-05, RN-06, RN-10 | HU-02, HU-03 | Lembrete 24 h e de última hora |
| P3 | RF-04 | RN-02 | HU-01 | Fim calculado pela duração-padrão |
| P4 | RF-01, RF-09, RF-10 | RN-09 | — (2ª fase) | Sugestão de retorno após o prazo |
| P5 | RF-07, RF-11 | RN-07 | HU-05 | Relatório de ocupação e faltas |

## Riscos

| # | Risco | Prob. | Impacto | Mitigação |
|---|-------|:-----:|:-------:|-----------|
| R1 | Tempos-padrão dos serviços mal estimados fazem a agenda estourar | Alta | Alto | Começar com valores da equipe e revisar mensalmente com a duração real registrada |
| R2 | Recepção continua marcando por fora do sistema | Média | Alto | Treinamento curto, uso obrigatório em um piloto de 2 semanas e acompanhamento diário |
| R3 | Clientes não respondem ao lembrete | Alta | Médio | Medir a taxa de resposta; RN-06 garante que a ausência de resposta não derruba o horário |
| R4 | Envio de mensagens depende de um provedor externo | Média | Médio | Tratar falha de envio, tentar de novo e avisar a recepção |
| R5 | Dados pessoais exigem conformidade com a LGPD | Média | Alto | Coletar o mínimo (RNF-04) e prever anonimização a pedido |

## Perguntas em aberto

1. O horário de funcionamento muda por dia da semana?
2. Um serviço pode ocupar mais de um box ao mesmo tempo (ex.: alinhamento e elevador)?
3. Quem pode cancelar um agendamento já confirmado pelo cliente?
