# Desafio Técnico - Desenvolvedor(a) Pleno (PHP/Laravel)

Bem-vindo(a)!

Neste desafio queremos avaliar sua habilidade de projetar e implementar uma **API REST** em **Laravel**, aplicando boas práticas de arquitetura, **SOLID** e **Clean Code**, além de integrar cache, filas e testes.

---

## Objetivo
Construir uma API para gerenciar **Consultas** e **Serviços Adicionais**, obedecendo às regras de negócio abaixo.

---

## Regras Obrigatórias

### Consultas
- Usuários autenticados podem criar, listar, visualizar, editar e cancelar suas consultas.  
- Campos obrigatórios da consulta:  
  - `user_id` — referência ao usuário que criou a consulta  
  - `title` — título ou descrição da consulta  
  - `scheduled_at` — data e hora da consulta  
  - `status` — `pending`, `confirmed`, `cancelled`  
- **Regra de negócio importante:** não é possível criar duas consultas no mesmo horário para o mesmo usuário.  

### Serviços Adicionais
- Cada consulta pode ter serviços adicionais opcionais, como “Material”, “Equipamento”, “Suporte Extra”.  
- Campos obrigatórios do serviço:  
  - `name` — nome do serviço  
  - `price` — valor decimal  
- Ao criar ou atualizar uma consulta, calcular o **total da consulta** somando o valor dos serviços adicionais.  

### Autenticação
- Usuários podem ser criados via **endpoint de registro** ou através de **seed** com credenciais padrão.  
- Todas as rotas de consultas e serviços devem exigir autenticação.  

---

## Requisitos técnicos obrigatórios
- **Laravel 11+**  
- **MySQL** (rodando via Docker)  
- **Redis** (rodando via Docker) para:  
  - Cache de listagem de consultas  
  - Filas para envio de e-mail ao criar ou atualizar consultas  
- **Docker + docker-compose** para subir o ambiente completo  
- Aplicação deve ser estruturada aplicando **SOLID e Clean Code** (ex: Services, Repositories ou Actions)   
- **Paginação** nas listagens  
- **README** completo explicando como rodar, seeds e credenciais  

---

## Diferenciais
- Laravel Resources para padronizar respostas da API  
- Validação completa de dados com Form Requests  
- Notificações via e-mail usando filas (Redis)  
- Documentação da API (Swagger ou Postman Collection)  
- Tratamento de exceções e erros de negócio de forma centralizada  
- Testes automatizados obrigatórios (unitários e/ou integração) 
---

## Entrega
1. Crie um repositório no GitHub (público ou privado).  
2. Suba seu código com histórico de commits claros.  
3. Envie o link para a nossa equipe.
