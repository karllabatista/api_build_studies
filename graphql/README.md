# Desafios práticos para treinar modelagem GraphQL

## Nível Iniciante — Modelagem básica

**Objetivo**:Treinar type, Query e relacionamentos simples (1:N).

1.**Catálogo de Filmes**

Tipos: Filme, Diretor, Gênero

Query: listar filmes, buscar por gênero, buscar diretor e seus filmes

Mutation: adicionar filme

Desafio extra: permitir filtro por nota ou ano de lançamento

-----------------------------------------------------------
2.**Sistema de Tarefas (To-do)**

Tipos: Usuario, Tarefa

Relacionamento: um usuário pode ter várias tarefas

Mutation: criar tarefa, marcar como concluída

Query: listar tarefas pendentes de um usuário


--------------------------------------

3. **Biblioteca Online**

Tipos: Livro, Autor, Categoria

Query: buscar livros por categoria, autor, título

Mutation: cadastrar livro/autor

Desafio extra: campo virtual que mostra a quantidade de livros por autor

--------------------------

# Nível Intermediário — Modelagem com múltiplas entidades e filtros

**Objetivo**: Trabalhar com N:N, filtros e paginação.

1.**Plataforma de Cursos**

Tipos: Curso, Instrutor, Aluno, Matricula

Query: buscar cursos com número de alunos, listar alunos por curso

Mutation: inscrever aluno em curso

**Desafio extra**: implementar paginação (limit, offset) nas queries

-----------------------------


2.**Rede Social Básica**

Tipos: Usuario, Post, Comentario, Like

Relacionamento: um post tem vários comentários e likes

Query: feed de posts recentes

Mutation: criar post, comentar, curtir

**Desafio extra**: resolver problema de n+1 queries com DataLoader

-------------------------------

3. **E-commerce Simplificado**

Tipos: Produto, Categoria, Carrinho, Pedido, Usuario

Query: listar produtos com filtro de categoria e preço

Mutation: adicionar item ao carrinho, fechar pedido

**Desafio extra:** incluir enum para status de pedido (PENDENTE, PAGO, ENVIADO)

-------------------------------------------

## 🧠 Nível Avançado — Modelagem com subschemas, fragmentos e directives

Objetivo: Treinar composição e modularização do schema.

**1. Plataforma de Streaming**

Tipos: Filme, Série, Episódio, Usuário, Avaliação

Union type: Midia = Filme | Serie

Query: buscar mídia por tipo

Directive customizada: @auth para proteger queries

Desafio extra: resolver filtros complexos (ex: “filmes com nota > 8 lançados após 2020”)

-----------------------------------------------

**2.Sistema de Reservas (Hotel/Voos)**

Tipos: Cliente, Reserva, Quarto, Pagamento

Mutation: reservar quarto, cancelar reserva, efetuar pagamento

Query: listar reservas ativas

Desafio extra: incluir lógica de disponibilidade dinâmica