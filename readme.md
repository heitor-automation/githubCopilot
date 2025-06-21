# Library App

## Descrição

O Library App é uma aplicação modular desenvolvida em .NET para gerenciar operações de biblioteca, como empréstimos de livros, cadastro de usuários e controle de inventário. O projeto segue a abordagem de Clean Architecture, promovendo escalabilidade, testabilidade e manutenção facilitada.

## Estrutura do Projeto

- `AZ2007LabAppM3.sln` – Arquivo de solução principal.
- `AccelerateDevGHCopilot/`
  - `src/`
    - `Library.ApplicationCore/`
      - `Entities/` – Entidades de domínio principais (ex: Book, Patron, Loan).
      - `Enums/` – Enumerações utilizadas na aplicação.
      - `Interfaces/` – Interfaces para abstrações do domínio.
      - `Services/` – Serviços e lógica de negócio.
      - `Library.ApplicationCore.csproj` – Projeto do núcleo da aplicação.
    - `Library.Console/`
      - `appSettings.json` – Configurações da aplicação console.
      - `CommonActions.cs`, `ConsoleApp.cs`, `ConsoleState.cs`, `Program.cs` – Lógica e fluxo da interface de linha de comando.
      - `Json/` – Utilitários ou dados em JSON.
      - `Library.Console.csproj` – Projeto da aplicação console.
    - `Library.Infrastructure/`
      - `Data/` – Implementações de acesso a dados.
      - `Library.Infrastructure.csproj` – Projeto da camada de infraestrutura.
  - `tests/`
    - `UnitTests/`
      - `LoanFactory.cs`, `PatronFactory.cs` – Fábricas para dados de teste.
      - `ApplicationCore/` – Testes unitários do núcleo da aplicação.
      - `UnitTests.csproj` – Projeto de testes unitários.

## Principais Classes e Interfaces

- **Entidades**
  - `Book` – Representa um livro.
  - `Patron` – Representa um usuário da biblioteca.
  - `Loan` – Representa um empréstimo.
- **Interfaces**
  - `IBookRepository` – Operações de dados para livros.
  - `IPatronRepository` – Operações de dados para usuários.
  - `ILoanService` – Gerenciamento de empréstimos.
- **Serviços**
  - `LoanService` – Lógica de negócio para empréstimos.
  - `NotificationService` – Notificações de empréstimos em atraso.

## Como Usar

1. Clone o repositório:
   ```bash
   git clone <repository-url>
   ```
2. Navegue até o diretório do projeto:
   ```bash
   cd AccelerateDevGHCopilot/src/Library.Console
   ```
3. Restaure as dependências e ferramentas do projeto:
   ```bash
   dotnet restore
   ```
4. Execute a aplicação:
   ```bash
   dotnet run
   ```
5. Siga as instruções na tela para usar o aplicativo.

## Contribuindo

Contribuições são bem-vindas! Por favor, siga estas etapas para contribuir:

1. Faça um fork do repositório.
2. Crie uma nova branch para sua feature ou correção:
   ```bash
   git checkout -b minha-feature
   ```
3. Faça suas alterações e commit:
   ```bash
   git commit -m 'Minha nova feature'
   ```
4. Envie para o repositório remoto:
   ```bash
   git push origin minha-feature
   ```
5. Abra um Pull Request.

## Licença

Este projeto está licenciado sob a Licença MIT - veja o arquivo [LICENSE](LICENSE) para detalhes.