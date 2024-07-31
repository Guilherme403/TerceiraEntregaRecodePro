# Agência de Viagens - Aplicação Web

Este projeto é uma aplicação web desenvolvida utilizando o ecossistema Spring Framework e tecnologias Java. O back-end é construído com Java Spring Boot, Spring MVC, e Spring Data JPA, com MySQL para persistência de dados. O front-end é baseado no padrão MVC e usa Thymeleaf para renderização das views.

## Tecnologias Utilizadas

- **Back-end**: Java Spring Boot, Spring MVC, Spring Data JPA
- **Banco de Dados**: MySQL
- **Front-end**: Thymeleaf
- **Manipulação de JSON**: Implementado para interações com APIs

## Estrutura do Projeto

### 1. Banco de Dados

A implementação do banco de dados utiliza MySQL e pode ser realizada manualmente ou através de ORM (Object-Relational Mapping).

#### Modelo Lógico do Banco de Dados

- **Destinos**
  - **id**: INT, AUTO_INCREMENT, PRIMARY KEY
  - **nome**: VARCHAR(255), NOT NULL
  - **valor**: DECIMAL(10, 2), NOT NULL

- **Usuários**
  - **cpf**: VARCHAR(11), PRIMARY KEY
  - **nome**: VARCHAR(255), NOT NULL
  - **email**: VARCHAR(255), NOT NULL, UNIQUE
  - **telefone**: VARCHAR(20)

#### Scripts SQL para Criação das Tabelas

```sql
CREATE TABLE destino (
    id INT AUTO_INCREMENT PRIMARY KEY,
    nome VARCHAR(255) NOT NULL,
    valor DECIMAL(10, 2) NOT NULL
);

CREATE TABLE usuario (
    cpf VARCHAR(11) PRIMARY KEY,
    nome VARCHAR(255) NOT NULL,
    email VARCHAR(255) NOT NULL UNIQUE,
    telefone VARCHAR(20)
);
