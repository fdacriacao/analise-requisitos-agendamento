# Análise de requisitos — agendamento de serviços para oficina

Documentação de requisitos de um sistema de agendamento, escrita como seria entregue a uma equipe de desenvolvimento: do problema de negócio aos critérios de aceite.

> **Caso didático e anonimizado.** Inspirado em um problema recorrente de oficinas e centros automotivos. Não contém dados de nenhuma empresa.

## O que este repositório demonstra

Competência de análise de negócios: transformar uma dor operacional em requisitos claros, rastreáveis e testáveis.

| Documento | Conteúdo |
|-----------|----------|
| [`01-contexto-e-problema.md`](01-contexto-e-problema.md) | Problema, objetivos, escopo, partes interessadas, indicadores de sucesso |
| [`02-requisitos.md`](02-requisitos.md) | Requisitos funcionais e não funcionais, priorizados (MoSCoW) |
| [`03-regras-de-negocio.md`](03-regras-de-negocio.md) | Regras numeradas (RN-01…) e casos-limite |
| [`04-historias-e-criterios-de-aceite.md`](04-historias-e-criterios-de-aceite.md) | Histórias de usuário com critérios de aceite em Dado/Quando/Então |
| [`05-modelo-de-dados.md`](05-modelo-de-dados.md) | Diagrama entidade-relacionamento (Mermaid) |
| [`06-rastreabilidade-e-riscos.md`](06-rastreabilidade-e-riscos.md) | Matriz requisito → história → regra, e riscos com mitigação |
| [`modelo/levantamento-de-requisitos.md`](modelo/levantamento-de-requisitos.md) | Roteiro de entrevista reutilizável para novos projetos |

## Método

1. **Entrevista** com quem opera o processo (recepção, mecânicos, gestão), guiada pelo roteiro em `modelo/`.
2. **Mapeamento do processo atual**, para achar onde o tempo e o dinheiro se perdem.
3. **Requisitos priorizados** por impacto no indicador de sucesso, e não por facilidade técnica.
4. **Regras de negócio separadas dos requisitos**, para que mudem sem reescrever o sistema.
5. **Critérios de aceite testáveis**, escritos antes do desenvolvimento.
6. **Rastreabilidade**: cada requisito aponta para a história e a regra que o sustentam.

## Transparência

Documento redigido com apoio de IA (Claude) e revisado por mim, a partir da experiência com levantamento de requisitos e implantação de sistemas.

## Autor

Filippe Daruis · Itaperuna/RJ · [LinkedIn](https://www.linkedin.com/in/filippe-daruis-1b227294/)
