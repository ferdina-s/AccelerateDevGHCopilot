# Library App

## Description

Library App is a modular .NET application for managing library operations such as tracking books, patrons, and loans. It features a clean architecture with separate layers for core logic, infrastructure, and a console-based user interface. Data is stored in JSON files for easy prototyping and testing.

## Project Structure

- AccelerateDevGHCopilot.sln
- src/
  - Library.ApplicationCore/
    - Entities/
    - Enums/
    - Interfaces/
    - Services/
    - Library.ApplicationCore.csproj
  - Library.Infrastructure/
    - Data/
    - Library.Infrastructure.csproj
  - Library.Console/
    - Json/
    - appSettings.json
    - CommonActions.cs
    - ConsoleApp.cs
    - ConsoleState.cs
    - Library.Console.csproj
    - Program.cs
- tests/
  - UnitTests/
    - ApplicationCore/
      - LoanService/
      - PatronService/
    - LoanFactory.cs
    - PatronFactory.cs
    - UnitTests.csproj

## Key Classes and Interfaces

- **Entities**: `Author`, `Book`, `BookItem`, `Loan`, `Patron` — Represent core domain objects.
- **Enums**: `LoanExtensionStatus`, `LoanReturnStatus`, `MembershipRenewalStatus` — Enumerations for domain logic.
- **Interfaces**: `ILoanRepository`, `ILoanService`, `IPatronRepository`, `IPatronService` — Abstractions for services and data access.
- **Services**: `LoanService`, `PatronService` — Business logic for loans and patrons.
- **Infrastructure**: `JsonData`, `JsonLoanRepository`, `JsonPatronRepository` — Data access and persistence using JSON files.
- **Console App**: `ConsoleApp`, `ConsoleState`, `CommonActions` — User interface and application flow.

## Usage

1. Build the solution using Visual Studio or `dotnet build`.
2. Run the console application:
   ```sh
   dotnet run --project src/Library.Console/Library.Console.csproj
   ```
3. Follow the on-screen prompts to interact with the library system.

## License

This project is licensed under the MIT License.
