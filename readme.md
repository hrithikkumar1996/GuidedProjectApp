# Library App

## Description
Library App is a sample console-based library management system. It allows users to search for patrons, view and manage book loans, and renew memberships. The application uses JSON files for data storage and demonstrates clean separation of concerns using repositories, services, and dependency injection.

## Project Structure
- GuidedProjectApp.sln
- AccelerateDevGitHubCopilot/
  - src/
    - Library.ApplicationCore/
      - Entities/
        - Author.cs
        - Book.cs
        - BookItem.cs
        - Loan.cs
        - Patron.cs
      - Enums/
        - EnumHelper.cs
        - LoanExtensionStatus.cs
        - LoanReturnStatus.cs
        - MembershipRenewalStatus.cs
      - Interfaces/
        - ILoanRepository.cs
        - ILoanService.cs
        - IPatronRepository.cs
        - IPatronService.cs
      - Services/
        - LoanService.cs
        - PatronService.cs
      - Library.ApplicationCore.csproj
    - Library.Console/
      - Program.cs
      - ConsoleApp.cs
      - ConsoleState.cs
      - CommonActions.cs
      - appSettings.json
      - Json/
        - Authors.json
        - Books.json
        - BookItems.json
        - Loans.json
        - Patrons.json
      - Library.Console.csproj
    - Library.Infrastructure/
      - Data/
        - JsonData.cs
        - JsonLoanRepository.cs
        - JsonPatronRepository.cs
      - Library.Infrastructure.csproj
  - tests/
    - UnitTests/
      - ApplicationCore/
        - LoanService/
        - PatronService/
      - LoanFactory.cs
      - PatronFactory.cs
      - UnitTests.csproj

## Key Classes and Interfaces
- **ConsoleApp**: Main controller for the console UI and user flow.
- **JsonData**: Handles loading, saving, and populating data from JSON files.
- **JsonPatronRepository, JsonLoanRepository**: Data access for patrons and loans.
- **LoanService, PatronService**: Business logic for loans and patrons.
- **Entities**: Author, Book, BookItem, Loan, Patron.
- **Enums**: EnumHelper, LoanExtensionStatus, LoanReturnStatus, MembershipRenewalStatus.
- **Interfaces**: ILoanRepository, ILoanService, IPatronRepository, IPatronService.

## Usage
1. Ensure you have [.NET 8.0 Runtime](https://dotnet.microsoft.com/en-us/download/dotnet/8.0) installed.
2. Place your data files in the `Json/` directory or use the provided samples.
3. Build and run the console app:
   ```sh
   dotnet run --project AccelerateDevGitHubCopilot/src/Library.Console/Library.Console.csproj
   ```
4. Follow the on-screen prompts to search for patrons, view details, manage loans, and renew memberships.

## License
This project is licensed under the MIT License.
