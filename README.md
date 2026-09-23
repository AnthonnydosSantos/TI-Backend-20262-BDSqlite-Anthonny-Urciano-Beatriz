# Geek Store — Banco de Dados SQLite

Projeto de banco de dados para uma loja geek, desenvolvido a partir do DER da equipe.

## Estrutura

### Tabelas principais
- CLIENTE
- PEDIDO
- ITEM_PEDIDO
- PRODUTO
- CATEGORIA

### Tabelas complementares
- ENDERECO
- AVALIACAO
- PAGAMENTO
- ENTREGA_FRETE
- FRETE
- ESTOQUE

## Relacionamentos

- CLIENTE 1:N PEDIDO
- CLIENTE 1:N ENDERECO
- CLIENTE 1:N AVALIACAO
- CATEGORIA 1:N PRODUTO
- PRODUTO 1:N ITEM_PEDIDO
- PEDIDO 1:N ITEM_PEDIDO
- PRODUTO 1:1 ESTOQUE
- PRODUTO 1:N AVALIACAO
- PEDIDO 1:1 PAGAMENTO
- PEDIDO 1:1 ENTREGA_FRETE
- FRETE 1:N ENTREGA_FRETE

## Status

### Status do pedido
- Pendente
- Em separação
- Enviado
- Entregue
- Cancelado

### Status do pagamento
- Pendente
- Aprovado
- Recusado
- Estornado

### Status da entrega
- Em preparação
- Em trânsito
- Entregue
- Atrasado
- Cancelado

## Arquivos

- `schema.sql` — criação das tabelas, PKs, FKs e restrições.
- `insert.sql` — inserção e população do banco.
- `queries.sql` — consultas SELECT, WHERE, ORDER BY, JOIN e agregações.
- `geek_store.db` — banco SQLite final já populado.
- `README.md` — documentação do projeto.

## Como executar

Com SQLite:

```sql
.read schema.sql
.read insert.sql
.read queries.sql
```

Ou abra diretamente o arquivo `geek_store.db` em um programa compatível com SQLite.

## GitHub

Sugestão de organização:

```text
geek-store-banco/
├── schema.sql
├── insert.sql
├── queries.sql
├── geek_store.db
└── README.md
```
