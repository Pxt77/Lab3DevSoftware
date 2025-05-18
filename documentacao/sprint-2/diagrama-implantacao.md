@startuml
skinparam nodeStyle rectangle
left to right direction

node "ClienteWeb" {
  component "Navegador"
}

node "ServidorAplicacao" {
  component "Módulo de Autenticação"
  component "Módulo de Transações"
  component "Módulo de Instituições"
  component "Módulo de Benefícios"
}

node "BancoDeDados" {
  component "Sistema de Banco de Dados"
}

"Navegador" --> "ServidorAplicacao" : HTTP

"ServidorAplicacao" --> "Sistema de Banco de Dados" : HTTP
@enduml
