# Vendas Online DB

Projeto desenvolvido para a disciplina de Banco de Dados do curso Técnico em Desenvolvimento de Sistemas do SENAI.

O objetivo do projeto é criar e manipular um banco de dados para um sistema de vendas online, utilizando SQL Server.

## Funcionalidades

O banco de dados possui as seguintes tabelas:

- Clientes
- Pedidos
- Entregas

Também foram utilizados:

- Chaves primárias
- Chaves estrangeiras
- Índices
- Inserção de dados
- Consultas SQL
- Views
- Funções de agregação
- INNER JOIN

## Estrutura do Banco

### Clientes

Armazena informações dos clientes, como:

- Nome
- CPF
- E-mail
- Cidade
- Status ativo

### Pedidos

Armazena os pedidos realizados pelos clientes, contendo:

- Cliente responsável pelo pedido
- Valor do pedido
- Data do pedido

### Entregas

Armazena informações sobre as entregas dos pedidos, contendo:

- Pedido relacionado
- Data da entrega
- Status
- Valor do frete

## Índices

Foram criados índices para melhorar o desempenho das consultas:

- `idx_cidade` na coluna `cidade` da tabela `clientes`
- `idx_data_pedido` na coluna `data_pedido` da tabela `pedidos`
- `idx_status` na coluna `status` da tabela `entregas`

## Views

### resumoEntregas

Apresenta um resumo das entregas, mostrando:

- Total de entregas
- Média do valor dos fretes

### entregasConcluidas

Mostra apenas as entregas com status `Entregue`.

A consulta utiliza `INNER JOIN` entre as tabelas `entregas` e `pedidos` para apresentar:

- ID do pedido
- Valor do pedido
- Valor do frete
- Data da entrega

## Tecnologias Utilizadas

- SQL
- SQL Server
- SQL Server Management Studio - SSMS

## Autor

Lukas Alves Gonçalves

Curso Técnico em Desenvolvimento de Sistemas  
SENAI Edward Savio - Jaú/SP
