# 03 · Regras de negócio

Regras ficam separadas dos requisitos para poderem mudar sem reescrever o sistema.

| ID | Regra | Relacionada a |
|----|-------|---------------|
| RN-01 | Um box só pode ter um agendamento por intervalo de tempo. Dois intervalos se sobrepõem se `inicio_A < fim_B` e `inicio_B < fim_A`. | RF-03 |
| RN-02 | `fim = inicio + duração-padrão do serviço`. O horário de fim não é digitado pelo usuário. | RF-04 |
| RN-03 | Há um intervalo de folga configurável entre agendamentos no mesmo box (padrão: 10 min). | RF-03 |
| RN-04 | Só se agenda dentro do horário de funcionamento. Serviço que ultrapasse o fechamento é recusado. | RF-02 |
| RN-05 | O lembrete é enviado 24 h antes, exceto se o agendamento foi criado com menos de 24 h de antecedência: nesse caso, é enviado na criação. | RF-05 |
| RN-06 | Cliente sem resposta ao lembrete mantém o status "agendado". O horário só é liberado por decisão da recepção, nunca automaticamente. | RF-06 |
| RN-07 | Falta sem aviso é marcada pela recepção após 30 min do horário e entra no histórico do cliente. | RF-07, RF-11 |
| RN-08 | Remarcação gera novo agendamento e cancela o anterior, mantendo o vínculo entre os dois para auditoria. | RF-06, RNF-06 |
| RN-09 | O retorno de revisão é sugerido quando passar o prazo configurado para o tipo de serviço (ex.: 6 meses). | RF-10 |
| RN-10 | Telefone é obrigatório para o envio de lembretes. Sem telefone, o agendamento é permitido, com aviso de que não haverá lembrete. | RF-01, RF-05 |

## Casos-limite

| Situação | Comportamento esperado |
|----------|------------------------|
| Dois usuários tentam o mesmo horário ao mesmo tempo | O sistema aceita o primeiro e informa o segundo; a verificação é feita no momento de gravar (RN-01) |
| Serviço que cruza o horário de almoço | Permitido se o box não tiver bloqueio configurado no intervalo |
| Cliente remarca 3 vezes | Permitido; a quantidade aparece no histórico para a gestão |
| Veículo trocado de dono | O histórico acompanha a placa; o vínculo com o cliente antigo é encerrado |
| Cliente pede exclusão dos dados (LGPD) | Dados pessoais são anonimizados; os registros de serviço permanecem sem identificação (RNF-04) |
