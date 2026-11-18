# 02 · Requisitos

Prioridade MoSCoW: **M**ust (essencial), **S**hould (importante), **C**ould (desejável), **W**on't (fora desta fase).

## Funcionais

| ID | Requisito | Prioridade | Resolve |
|----|-----------|:----------:|:-------:|
| RF-01 | Cadastrar cliente (nome, telefone) e veículo (placa, modelo, ano) | M | P4 |
| RF-02 | Criar agendamento escolhendo serviço, box, data e hora | M | P1 |
| RF-03 | Bloquear agendamento que se sobreponha a outro no mesmo box | M | P1 |
| RF-04 | Calcular a duração do agendamento pelo tempo-padrão do serviço | M | P3 |
| RF-05 | Enviar lembrete ao cliente antes do horário (ex.: 24 h) | M | P2 |
| RF-06 | Permitir ao cliente confirmar ou remarcar pela mensagem | S | P2 |
| RF-07 | Registrar status: agendado, confirmado, em atendimento, concluído, faltou, cancelado | M | P5 |
| RF-08 | Exibir agenda por box e por dia | M | P1 |
| RF-09 | Manter histórico de serviços por veículo | S | P4 |
| RF-10 | Sugerir retorno de revisão conforme o último serviço | C | P4 |
| RF-11 | Relatório de ocupação e de faltas por período | S | P5 |
| RF-12 | Fila de espera: oferecer horário vago a quem aguarda | C | P2 |
| RF-13 | Cobrança e emissão fiscal | W | — |

## Não funcionais

| ID | Requisito | Prioridade |
|----|-----------|:----------:|
| RNF-01 | Criar um agendamento em até 3 passos na tela | M |
| RNF-02 | Funcionar em celular e computador (responsivo) | M |
| RNF-03 | Resposta de consulta de agenda em até 2 s no uso normal | S |
| RNF-04 | Tratar dados pessoais conforme a LGPD: finalidade, minimização e possibilidade de exclusão | M |
| RNF-05 | Acesso por perfil: recepção, mecânico e gestão veem apenas o necessário | M |
| RNF-06 | Registro de auditoria de criação, alteração e cancelamento de agendamentos | S |
| RNF-07 | Cópia de segurança diária dos dados | M |
