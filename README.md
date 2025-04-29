<h1 align="center">🧩 Nest Clean Domain</h1>

<p align="center"><i>Camada de <b>Domínio</b> independente e desacoplada, desenvolvida seguindo os princípios do <b>DDD</b> (Domain-Driven Design), para modelar regras de negócio de forma clara, consistente e reutilizável.</i>
  <!-- <br/><br/>
  <img src="https://img.shields.io/github/last-commit/joschonarth/node-clean-domain?style=for-the-badge&color=EA284C&labelColor=1C1E26" alt="last-commit">
  <img src="https://img.shields.io/github/languages/top/joschonarth/node-clean-domain?style=for-the-badge&color=EA284C&labelColor=1C1E26" alt="top-language">
  <img src="https://img.shields.io/github/languages/count/joschonarth/node-clean-domain?style=for-the-badge&color=EA284C&labelColor=1C1E26" alt="languages-count"> -->
</p>

## 📑 Índice

- [📖 Visão Geral](#-visão-geral)
- [🛠️ Tecnologias Utilizadas](#️-tecnologias-utilizadas)
- [⚙️ Conceitos Aplicados](#️-conceitos-aplicados)
<!-- - [🚀 Como Executar o Projeto](#-como-executar-o-projeto)
  - [📋 Pré-requisitos](#-pré-requisitos)
  - [🔧 Instalação](#-instalação)
  - [▶️ Execução](#️-execução) -->
- [🧪 Testes](#-testes)
- [🤝 Contribuições](#-contribuições)
- [⭐ Apoie este Projeto](#-apoie-este-projeto)
- [📞 Contato](#-contato)

## 📖 Visão Geral

Este projeto representa a camada de domínio de uma aplicação construída com NestJS e arquitetura limpa.

Responsável por centralizar as regras de negócio, o domínio é totalmente independente de frameworks e infraestrutura, tornando-o reutilizável, testável e manutenível.

A modelagem foi feita com base nos princípios do Domain-Driven Design (DDD), focando em representar fielmente as operações essenciais de um fórum: gerenciamento de usuários, tópicos, posts, respostas e comentários.

## 🛠️ Tecnologias Utilizadas

- 🟢 **Node.js**: Plataforma para execução do JavaScript no servidor.
- 🟦 **TypeScript**: Tipagem estática para segurança e escalabilidade.
- 🧪 **Vitest**: Testes de unidade para garantir a integridade das regras de negócio.
- 🧩 **Zod**: Validação de entidades e objetos de valor.
- ⚙️ **ESLint**: Padronização e qualidade de código.

## ⚙️ Conceitos Aplicados

- 📚 Domain-Driven Design (DDD): Foco no domínio de negócio como núcleo da aplicação.
- 🛡️ Clean Architecture: Separação de responsabilidades e independência de frameworks.
- 🧱 Entidades e Objetos de Valor: Organização robusta de dados e comportamentos.
- 🧩 Repositórios como Contratos: Persistência desacoplada e flexível.
- 🧪 TDD: Desenvolvimento orientado a testes desde o início.
- 🧹 SOLID: Aplicação de princípios para alta manutenibilidade e extensibilidade.

## 🌐 Relação com a API

Esta camada **Domain** é utilizada pela aplicação que expõe a **API**, responsável por disponibilizar os recursos para consumo externo.
A aplicação da **API** utiliza as entidades e regras definidas no **Domain** para realizar suas operações de forma consistente.

Você pode acessar o repositório da API aqui: [Nest Clean API](https://github.com/joschonarth/nest-clean-api)

## 🧪 Testes

Este projeto inclui **testes unitários** para garantir a confiabilidade e o funcionamento correto dos recursos implementados. Para executar os testes, utilize os seguintes comandos:

- **Executar testes unitários:**

  ```bash
  npm run test
  ```

- **Executar testes unitários em modo de observação:**

  ```bash
  npm run test:watch
  ```

## 🤝 Contribuições

Contribuições são muito bem-vindas! Sinta-se à vontade para abrir issues ou pull requests com melhorias ou correções. 🚀

## ⭐ Apoie este Projeto

Se você gostou da aplicação, deixe uma ⭐ no repositório!

## 📞 Contato

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/joschonarth/)
[![Gmail](https://img.shields.io/badge/Gmail-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:joschonarth@gmail.com)
