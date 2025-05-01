<h1 align="center">🧩 Nest Clean Domain</h1>

<p align="center"><i>Camada de <b>Domínio</b> independente e desacoplada, desenvolvida seguindo os princípios do <b>Domain-Driven Design</b> e da <b>Clean Architecture</b>, para modelar regras de negócio de forma clara, consistente e reutilizável.</i></p>

## 📑 Índice

- [📖 Visão Geral](#-visão-geral)
- [🛠️ Tecnologias Utilizadas](#️-tecnologias-utilizadas)
- [⚙️ Funcionalidades](#️-funcionalidades)
- [📚 Conceitos Aplicados](#-conceitos-aplicados)
- [🗂️ Estrutura do Projeto](#️-estrutura-do-projeto)
- [🧪 Testes](#-testes)
- [🌐 Relação com a API](#-relação-com-a-api)
- [🤝 Contribuições](#-contribuições)
- [⭐ Apoie este Projeto](#-apoie-este-projeto)
- [📞 Contato](#-contato)

## 📖 Visão Geral

Este projeto representa a camada de domínio de uma aplicação construída com base nos princípios do **Domain-Driven Design (DDD)** e da **Clean Architecture**.

Responsável por centralizar as regras de negócio, o domínio é totalmente independente de frameworks e infraestrutura, tornando-o reutilizável, testável e manutenível.

A modelagem segue os fundamentos do **DDD**, com foco em refletir com fidelidade os processos centrais de um fórum, como o gerenciamento de usuários, tópicos, postagens, respostas e comentários.

## 🛠️ Tecnologias Utilizadas

- 🟢 **Node.js**: Plataforma para execução do JavaScript no servidor.
- 🟦 **TypeScript**: Tipagem estática para segurança e escalabilidade.
- 🧪 **Vitest**: Testes de unidade para garantir a integridade das regras de negócio.
- 🧩 **Zod**: Validação de entidades e objetos de valor.
- ⚙️ **ESLint**: Padronização e qualidade de código.

## ⚙️ Funcionalidades

- 📝 **Criação e gestão de perguntas**: Usuários podem criar, editar e excluir suas próprias perguntas no fórum.
- 💬 **Sistema de respostas**: Respostas podem ser adicionadas a perguntas e editadas ou excluídas posteriormente.
- 🗨️ **Sistema de comentários**: Comentários podem ser adicionados a perguntas e respostas, além de poderem ser editados ou excluídos.
- 🏆 **Escolha da melhor resposta**: O autor de uma pergunta pode marcar uma resposta como a melhor solução.
- 🔍 **Busca de perguntas e respostas**: Permite consultar perguntas recentes, respostas e seus respectivos comentários.
- 🗑️ **Gerenciamento de conteúdo**: Permite a exclusão de perguntas, respostas e comentários específicos.

## 📚 Conceitos Aplicados

- 🧩 **Domain-Driven Design (DDD)**: Foco no domínio de negócio como núcleo da aplicação.
- 🛡️ **Clean Architecture**: Separação de responsabilidades e independência de frameworks.
- 🧱 **Entidades e Value Objects**: Organização robusta de dados e comportamentos.
- 🧩 **Repositórios como Contratos**: Persistência desacoplada e flexível.
- 🧹 **SOLID**: Aplicação de princípios para alta manutenibilidade e extensibilidade.
- 🧪 **TDD (Test-Driven Development)**: Desenvolvimento orientado a testes desde o início.
- 🔄 **In-Memory Repository**: Repositório volátil usado para testes e simulações sem dependência externa.
- 🏭 **Factory Pattern**: Criação estruturada de objetos para testes ou instâncias complexas.
- 🧠 **Design Patterns**: Aplicação de padrões de projeto para promover reutilização, flexibilidade e clareza na modelagem.
- 🌐 **Domain Events**: Comunicação entre partes do sistema através de eventos explícitos do domínio.
- 🔗 **Aggregate Root**: Entidades raiz que garantem a integridade e consistência de um agregado.
- 📜 **Watched List**: Lista observável usada para rastrear mudanças em coleções (ex: notificações de alterações).
- ↔️ **Either**: Abordagem funcional para tratamento explícito de erros e retornos esperados.

## 🗂️ Estrutura do Projeto

A estrutura do projeto está organizada com foco em **modularidade**, **separação de responsabilidades** e adesão à **Clean Architecture**. A seguir, um panorama das principais pastas e seus propósitos:

```plaintext
nest-clean-domain/
├── src/
│   ├── core/                          # Camada genérica e compartilhada entre os domínios
│   │   ├── entities/                  # Entidades base como AggregateRoot e WatchedList
│   │   ├── errors/                    # Erros e exceções globais do domínio
│   │   ├── events/                    # Eventos de domínio genéricos
│   │   ├── repositories/              # Contratos genéricos de repositórios
│   │   ├── types/                     # Tipos utilitários
│   ├── domain/                        # Camadas específicas por contexto de domínio
│   │   ├── forum/
│   │   │   ├── application/           # Casos de uso e interfaces da camada de domínio
│   │   │   │   ├── repositories/      # Contratos específicos de repositórios para o fórum
│   │   │   │   └── use-cases/         # Casos de uso do fórum
│   │   │   ├── enterprise/            # Entidades e regras de negócio específicas do fórum
│   │   │   │   ├── entities/          # Entidades
│   │   │   │   │   └── value-objects/ # Objetos de valor do domínio fórum
│   │   │   │   └── events/            # Eventos específicos do domínio fórum
│   │   ├── notification/
│   │   │   ├── application/           # Camada de aplicação do domínio de notificações
│   │   │   │   ├── repositories/      # Contratos de persistência para notificações
│   │   │   │   ├── subscribers/       # Assinantes de eventos
│   │   │   │   └── use-cases/         # Casos de uso para notificações
│   │   │   └── enterprise/            # Entidades do domínio de notificações
│   │   │       └── entities/
├── test/
│   ├── factories/                     # Fábricas para criação de entidades e objetos de teste
│   ├── repositories/                  # Implementações in-memory dos repositórios para testes
│   └── utils/                         # Utilitários de suporte aos testes
```

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

## 🌐 Relação com a API

Esta camada **Domain** é utilizada pela aplicação que expõe a **API**, responsável por disponibilizar os recursos para consumo externo.
A aplicação da **API** utiliza as entidades e regras definidas no **Domain** para realizar suas operações de forma consistente.

👉 Você pode acessar o repositório da API [aqui](https://github.com/joschonarth/nest-clean-api).

## 🤝 Contribuições

Contribuições são muito bem-vindas! Sinta-se à vontade para abrir issues ou pull requests com melhorias ou correções. 🚀

## ⭐ Apoie este Projeto

Se você gostou da aplicação, deixe uma ⭐ no repositório!

## 📞 Contato

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/joschonarth/)
[![Gmail](https://img.shields.io/badge/Gmail-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:joschonarth@gmail.com)
