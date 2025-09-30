# Desafio Técnico - Desenvolvedor(a) Júnior (PHP/Laravel)

Bem-vindo(a)!

Neste desafio queremos avaliar sua habilidade de projetar e implementar uma **API REST** em **Laravel**. Foque em clareza, organização e funcionamento correto das regras de negócio abaixo.

---

## 🎯 Objetivo
Construir uma API para gerenciar **Produtos** e **Pedidos**, obedecendo às regras de negócio descritas neste documento.

---

## 📌 Regras Obrigatórias

### Produtos
- Todas as rotas são **públicas** (qualquer pessoa pode criar, editar, listar e excluir um produto).  
- Campos obrigatórios:  
  - `nome` (string)  
  - `preco` (decimal)  
  - `estoque` (inteiro)  
  - `categoria` (string)  
- **Restrição:** não é permitido **excluir** um produto que já esteja presente em qualquer pedido.  

### Pedidos
- Todas as rotas de pedidos **precisam de autenticação**.  
- Somente o **usuário que criou** um pedido pode:  
  - **Visualizar** o pedido.  
  - **Editar** o pedido.  
  - **Cancelar** o pedido (alterando o status para `cancelled`).  
- Não permitir exclusão definitiva de pedidos.  

---

## 🔐 Autenticação
- Você pode implementar de duas formas:  
  - Criando endpoints de **registro**, ou  
  - Fornecendo um **seeder** com usuário e senha padrão para a rota de **login** para testes.  

---

## 🛠️ Requisitos técnicos obrigatórios
- **Laravel 11+**  
- **MySQL**  
- **README** do projeto bem estruturado (como rodar, migrations, seeds, como obter credenciais se houver seed)  
- **Paginação** nas listagens  

---

## 🚀 Diferenciais (não obrigatórios, valorizados)
- Testes automatizados (PHPUnit / Pest).  
- Docker + docker-compose para facilitar subida do ambiente.  
- Redis (cache de listagem ou filas).  
- Uso de Laravel Resources para padronizar respostas.  
- Validação e decremento de estoque ao criar/editar pedidos (tratamento de estoque insuficiente).  

---

## 📦 Entrega
1. Crie um repositório no GitHub (público ou privado).  
2. Suba seu código com histórico de commits (commits claros são valorizados).  
3. Envie o link para a nossa equipe.  
