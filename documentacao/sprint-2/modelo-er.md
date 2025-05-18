# Modelo Entidade-Relacionamento (ER)

## Entidades Principais

### Aluno
- id (PK)
- nome
- email
- cpf
- rg
- endereco
- curso
- instituicao_id (FK)

### Professor
- id (PK)
- nome
- cpf
- departamento
- instituicao_id (FK)
- saldo_moedas

### Instituicao
- id (PK)
- nome
- cnpj

### Empresa
- id (PK)
- nome
- email
- cnpj

### Vantagem
- id (PK)
- nome
- descricao
- foto_url
- custo_moedas
- empresa_id (FK)

### Transacao
- id (PK)
- remetente_id (FK - Professor)
- destinatario_id (FK - Aluno)
- valor
- descricao
- data_hora

### Usuario
- id (PK)
- login
- senha
- tipo_usuario (enum: aluno, professor, empresa)
- referencia_id (FK - depende do tipo)

## Relacionamentos
- Aluno pertence a uma Instituicao
- Professor pertence a uma Instituicao
- Empresa oferece muitas Vantagens
- Vantagem pertence a uma Empresa
- Transacao envolve Professor e Aluno
