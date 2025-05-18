# Estratégia de Acesso a Dados

## Padrão Arquitetural
Utilizaremos o padrão DAO (Data Access Object) em conjunto com um ORM (Object-Relational Mapping).

## ORM Selecionado
Hibernate (caso Java) ou Sequelize (caso Node.js com Sequelize ORM).

## Justificativa
O uso do ORM garante:
- Facilidade de manutenção
- Redução do uso direto de SQL
- Melhor integração com o modelo de classes

## Estrutura DAO
Cada entidade terá um DAO correspondente:
- AlunoDAO
- ProfessorDAO
- EmpresaParceiraDAO
- VantagemDAO
- TransacaoDAO
- UsuarioDAO

Esses DAOs terão métodos padrão como:
- salvar()
- atualizar()
- remover()
- buscarPorId()
- listarTodos()

As regras de negócio serão mantidas em uma camada de serviço (Service Layer), desacoplando o acesso ao banco da lógica da aplicação.
