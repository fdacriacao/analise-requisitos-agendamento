# 01 · Contexto e problema

## Situação atual

Uma oficina de médio porte controla seus horários em papel e em mensagens de WhatsApp. A recepção anota o pedido, confere a disponibilidade de memória e confirma por mensagem.

## Problemas identificados

| # | Problema | Efeito no negócio |
|---|----------|-------------------|
| P1 | Dois clientes marcados para o mesmo horário e box | Fila, retrabalho e cliente insatisfeito |
| P2 | Cliente esquece o horário marcado | Box ocioso e receita perdida (falta sem aviso) |
| P3 | Duração do serviço estimada "de cabeça" | Agenda estoura; atrasos em cascata |
| P4 | Sem histórico por veículo | Retornos de revisão não são oferecidos |
| P5 | Gestão não sabe a taxa de ocupação | Decisões de equipe e horário sem dado |

## Objetivos

1. Eliminar conflitos de horário (P1).
2. Reduzir faltas sem aviso com lembretes automáticos (P2).
3. Dimensionar a agenda pela duração real de cada serviço (P3).
4. Manter histórico por veículo e sugerir retorno (P4).
5. Dar visibilidade de ocupação à gestão (P5).

## Indicadores de sucesso

| Indicador | Como medir | Meta ilustrativa |
|-----------|-----------|------------------|
| Conflitos de agenda por mês | Contagem de agendamentos sobrepostos | 0 |
| Taxa de faltas sem aviso | Faltas ÷ agendamentos | Reduzir pela metade em 3 meses |
| Ocupação dos boxes | Horas agendadas ÷ horas disponíveis | Acompanhar, sem meta fixa na 1ª fase |
| Retornos de revisão agendados | Retornos ÷ veículos atendidos | Crescimento mês a mês |

> As metas são ilustrativas. Em um projeto real, são definidas com a gestão após medir a linha de base.

## Escopo

**Dentro:** agendamento, confirmação e lembrete ao cliente, cadastro de cliente e veículo, tempos-padrão por serviço, visão de agenda por box, relatório de ocupação.

**Fora (1ª fase):** pagamento, emissão fiscal, estoque de peças, aplicativo móvel nativo.

## Partes interessadas

| Papel | Interesse principal |
|-------|---------------------|
| Recepção | Marcar rápido, sem conflito |
| Mecânicos | Ver o que vão atender e quanto tempo têm |
| Gestão | Ocupação, faltas e retornos |
| Cliente | Confirmar e remarcar sem ligar |
