# Projeto da Oficina Mecânica  

## Descrição  
Este projeto é um sistema de controle e gerenciamento de ordens de serviço para uma oficina mecânica.  
 
## 1. Identificação das Entidades
As entidades principais podem incluir:

👨‍💻Cliente

🚗Veículo

📝Ordem de Serviço (OS)

👨‍🔧Mecânico

👾Serviço

## 2. Definição dos Atributos
## 👨‍💻Cliente
id_cliente (PK)

nome

telefone

email

endereço

## 🚗Veículo
id_veiculo (PK)

modelo

marca

ano

placa

id_cliente (FK)

## 📝Ordem de Serviço (OS)
id_os (PK)

data_abertura

data_entrega

status (ex: em andamento, concluída)

id_veiculo (FK)

id_mecanico (FK)

## 👨‍🔧Mecânico
id_mecanico (PK)

nome

especialidade

telefone

## 👾Serviço
id_servico (PK)

descrição

preço

id_os (FK)

## 3. Definição dos Relacionamentos
Cliente - Veículo: Um cliente pode ter vários veículos, mas cada veículo pertence a um cliente.

Relacionamento: 1:N (Um para Muitos)

Veículo - Ordem de Serviço: Um veículo pode ter várias ordens de serviço, mas cada ordem de serviço refere-se a um único veículo.

Relacionamento: 1:N (Um para Muitos)

Ordem de Serviço - Mecânico: Uma ordem de serviço pode ser executada por um ou mais mecânicos, e um mecânico pode trabalhar em várias ordens de serviço.

Relacionamento: N:M (Muitos para Muitos)

Ordem de Serviço - Serviço: Uma ordem de serviço pode incluir vários serviços, e cada serviço pode ser parte de várias ordens de serviço.

Relacionamento: N:M (Muitos para Muitos)

## 4. Diagrama ER (Entidade-Relacionamento)
Com as entidades, atributos e relacionamentos definidos, você pode usar uma ferramenta para criar um Diagrama ER. O diagrama ajudará a visualizar as entidades e seus relacionamentos.

## Exemplo de Diagrama Simplificado

Cliente (1) ———— (N) Veículo

Veículo (1) ———— (N) Ordem de Serviço

Ordem de Serviço (N) ———— (M) Mecânico

Ordem de Serviço (N) ———— (M) Serviço
