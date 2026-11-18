# 04 · Histórias de usuário e critérios de aceite

## HU-01 · Agendar um serviço sem conflito
**Como** recepcionista, **quero** marcar um serviço escolhendo box, data e hora, **para** não duplicar horários.

```gherkin
Cenário: agendamento em horário livre
  Dado que o Box 1 está livre amanhã às 09:00
  Quando eu agendo "Revisão" (duração-padrão 60 min) no Box 1 às 09:00
  Então o agendamento é criado com fim às 10:00
  E o Box 1 fica ocupado das 09:00 às 10:00

Cenário: conflito de horário
  Dado que o Box 1 tem um agendamento das 09:00 às 10:00
  Quando eu tento agendar outro serviço no Box 1 às 09:30
  Então o sistema recusa o agendamento
  E informa o próximo horário livre do Box 1

Cenário: respeito à folga entre agendamentos
  Dado que a folga configurada é de 10 minutos
  E o Box 1 tem um agendamento até as 10:00
  Quando eu agendo no Box 1 às 10:05
  Então o sistema recusa e sugere 10:10
```
**Requisitos:** RF-02, RF-03, RF-04 · **Regras:** RN-01, RN-02, RN-03

## HU-02 · Lembrar o cliente
**Como** gestor, **quero** que o cliente receba um lembrete, **para** reduzir faltas sem aviso.

```gherkin
Cenário: lembrete 24 horas antes
  Dado um agendamento para amanhã às 14:00 com telefone cadastrado
  Quando chega o horário de envio (hoje às 14:00)
  Então o cliente recebe a mensagem de lembrete com data, hora e opções "confirmar" e "remarcar"

Cenário: agendamento de última hora
  Dado que eu crio um agendamento para daqui a 3 horas
  Então o lembrete é enviado imediatamente

Cenário: cliente sem telefone
  Dado um cliente sem telefone cadastrado
  Quando eu salvo o agendamento
  Então o sistema permite salvar
  E exibe o aviso "este cliente não receberá lembrete"
```
**Requisitos:** RF-05, RF-06 · **Regras:** RN-05, RN-06, RN-10

## HU-03 · Confirmar ou remarcar pela mensagem
**Como** cliente, **quero** responder ao lembrete, **para** confirmar ou mudar o horário sem ligar.

```gherkin
Cenário: confirmação
  Dado um lembrete enviado
  Quando o cliente responde "confirmar"
  Então o status muda para "confirmado"

Cenário: remarcação
  Dado um lembrete enviado
  Quando o cliente escolhe "remarcar" e um novo horário livre
  Então o agendamento antigo é cancelado
  E um novo é criado, vinculado ao anterior
```
**Requisitos:** RF-06, RF-07 · **Regras:** RN-08

## HU-04 · Ver a agenda do dia
**Como** mecânico, **quero** ver os atendimentos do meu box no dia, **para** me organizar.

```gherkin
Cenário: agenda por box
  Dado que existem 5 agendamentos hoje no Box 2
  Quando eu abro a agenda do Box 2
  Então vejo os 5 em ordem de horário, com serviço, veículo e duração prevista
```
**Requisitos:** RF-08 · **Regras:** RN-02

## HU-05 · Acompanhar ocupação e faltas
**Como** gestor, **quero** um relatório por período, **para** decidir equipe e horários.

```gherkin
Cenário: relatório de ocupação
  Dado um período selecionado
  Quando eu gero o relatório
  Então vejo, por box, horas agendadas, horas disponíveis e a taxa de ocupação
  E o total de faltas sem aviso do período
```
**Requisitos:** RF-11 · **Regras:** RN-07
