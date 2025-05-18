# Diagrama de Implantação (Texto Descritivo)

## Componentes do Sistema

- Front-end: Aplicação web em React
- Back-end: API RESTful (Node.js/Express ou Spring Boot)
- Banco de Dados: MySQL ou PostgreSQL
- Serviços de Email: SMTP (ex: SendGrid)
- Armazenamento de Imagens: AWS S3 ou local
- Autenticação: JWT (JSON Web Token)

## Infraestrutura

```
[Usuário]
   |
[Front-end React]
   |
[API Back-end - Autenticação, Regras de Negócio, DAO]
   |
[MySQL/PostgreSQL]
   |
[SMTP e S3 para envio de emails e imagens]
```

## Observações

- As imagens de vantagens serão armazenadas via link externo.
- Todos os dados sensíveis serão protegidos via autenticação.
- O sistema é distribuído em camadas (MVC) para facilitar manutenção e escalabilidade.
