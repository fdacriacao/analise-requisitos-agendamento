# 05 · Modelo de dados

```mermaid
erDiagram
    CLIENTE ||--o{ VEICULO : possui
    CLIENTE ||--o{ AGENDAMENTO : realiza
    VEICULO ||--o{ AGENDAMENTO : recebe
    SERVICO ||--o{ AGENDAMENTO : define
    BOX ||--o{ AGENDAMENTO : aloca
    AGENDAMENTO ||--o{ LEMBRETE : dispara
    AGENDAMENTO |o--o| AGENDAMENTO : remarcado_de

    CLIENTE {
        int id PK
        string nome
        string telefone
    }
    VEICULO {
        int id PK
        int cliente_id FK
        string placa
        string modelo
        int ano
    }
    SERVICO {
        int id PK
        string nome
        int duracao_padrao_min
        int prazo_retorno_dias
    }
    BOX {
        int id PK
        string nome
    }
    AGENDAMENTO {
        int id PK
        int cliente_id FK
        int veiculo_id FK
        int servico_id FK
        int box_id FK
        datetime inicio
        datetime fim
        string status
        int remarcado_de_id FK
    }
    LEMBRETE {
        int id PK
        int agendamento_id FK
        datetime enviado_em
        string resposta
    }
```

## Decisões de modelagem

- `fim` é gravado (e não só calculado) para permitir a verificação de sobreposição direto no banco.
- `status` assume os valores de RF-07. Uma tabela de apoio é desnecessária enquanto a lista for curta.
- `remarcado_de_id` guarda o vínculo entre agendamentos (RN-08), preservando a auditoria.
- `duracao_padrao_min` fica em `SERVICO`, e não no agendamento, para que a mudança de tempo-padrão não altere o passado: o `fim` já foi gravado.
- Para impedir sobreposição mesmo sob concorrência (caso-limite de 2 usuários simultâneos), a regra RN-01 deve ser garantida na gravação, por restrição no banco ou transação com bloqueio, e não apenas na tela.
