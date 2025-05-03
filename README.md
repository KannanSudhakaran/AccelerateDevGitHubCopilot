comming sooln
# Library App

## Description
Library App is a console-based application for managing library operations, including patron management, book loans, and membership renewals. It uses a JSON-based data storage system and follows a clean architecture with separate layers for application core, infrastructure, and user interface.

## Project Structure
- `AccelerateDevGitHubCopilot.sln`: Solution file for the project.
- `src/`
  - `Library.ApplicationCore/`
    - `Entities/`: Contains domain models such as `Patron`, `Loan`, `Book`, and `Author`.
    - `Enums/`: Defines enumerations like `MembershipRenewalStatus`, `LoanReturnStatus`, and `LoanExtensionStatus`.
    - `Interfaces/`: Contains interfaces for services and repositories, such as `IPatronService` and `ILoanRepository`.
    - `Services/`: Implements business logic, including `PatronService` and `LoanService`.
    - `Library.ApplicationCore.csproj`: Project file for the application core.
  - `Library.Console/`
    - `appSettings.json`: Configuration file for JSON data paths.
    - `CommonActions.cs`: Defines common actions for the console application.
    - `ConsoleApp.cs`: Main application class that manages the console interface and application state.
    - `ConsoleState.cs`: Enum for managing application states.
    - `Json/`: Contains JSON files for data storage (e.g., `Patrons.json`, `Loans.json`).
    - `Library.Console.csproj`: Project file for the console application.
    - `Program.cs`: Entry point for the console application.
  - `Library.Infrastructure/`
    - `Data/`: Contains data access classes like `JsonData`, `JsonPatronRepository`, and `JsonLoanRepository`.
    - `Library.Infrastructure.csproj`: Project file for the infrastructure layer.
- `tests/`
  - `UnitTests/`: Contains unit tests for the application.
    - `LoanFactory.cs`: Helper class for creating test loan objects.
    - `PatronFactory.cs`: Helper class for creating test patron objects.
    - `ApplicationCore/`: Contains tests for core services like `PatronService` and `LoanService`.
    - `UnitTests.csproj`: Project file for the unit tests.

## Key Classes and Interfaces
- **Application Core**
  - `Patron`: Represents a library patron.
  - `Loan`: Represents a book loan.
  - `IPatronService`: Interface for patron-related operations.
  - `ILoanService`: Interface for loan-related operations.
  - `PatronService`: Implements membership renewal logic.
  - `LoanService`: Implements loan return and extension logic.
- **Infrastructure**
  - `JsonData`: Manages JSON-based data storage.
  - `JsonPatronRepository`: Handles data access for patrons.
  - `JsonLoanRepository`: Handles data access for loans.
- **Console**
  - `ConsoleApp`: Main class for managing the console interface and application state.
  - `CommonActions`: Enum for user actions in the console application.
  - `ConsoleState`: Enum for application states.

## Usage
1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd <repository-folder>