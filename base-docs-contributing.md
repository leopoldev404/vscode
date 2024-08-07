# Contributing

## Table of Contents
1. [Getting Started](#getting-started)
2. [Code Style Guidelines](#code-style-guidelines)
3. [Commit Message Guidelines](#commit-message-guidelines)
4. [Branching and Pull Requests](#branching-and-pull-requests)
5. [Testing](#testing)
6. [Issue Reporting](#issue-reporting)

---

## Getting Started
1. Fork the repository.
2. Clone your fork.
    ```sh
    git clone https://github.com/your-username/project-name.git
    ```
3. Navigate to the project directory.
    ```sh
    cd project-name
    ```
4. Install dependencies.
    ```sh
    [command to install dependencies]
    ```

## Code Style Guidelines
- Write clean, readable, and maintainable code.
- Prefer readability and simplicity over syntactic sugar.
- Follow the [Microsoft C# Coding Conventions](https://docs.microsoft.com/en-us/dotnet/csharp/fundamentals/coding-style/coding-conventions).
- Use meaningful names for variables, methods, and classes.
- Always use curly braces syntax.
- Prefer declaring variable types over `var` keyword.
- Use `var` only if variable type is no-ambiguos.
- Do not hard code literal values or magic number.
- Always use last available packages and features.

## Commit Message Guidelines
- Use the format `type(scope): message`.
    - **type**: The kind of change (e.g., `feat`, `fix`, `refac`).
    - **scope**: The module or component that has been changed (e.g., `dal`, `bl`, `web`, `api`, `common`).
    - **message**: A short, clear description of the change.
- Example commit messages:
    ```plaintext
    feat(dal): add get method
    fix(common): update scheduler configuration with new values 
    refac(bl): remove unused imports | remove unused packages
    ```

## Development Workflow
1. Create userstory
2. Add tasks to determine what is the scope of your user story
3. Create a new branch indicating the user story number.
    ```sh
    git switch -c feat/12345-your-feature-name
    ```
4. Make your changes.
5. Ensure all tests pass.
6. Commit your changes using the specified [commit message format](#commit-message-guidelines).
7. Push your branch.
    ```sh
    git push origin feat/your-feature-name
    ```
8. Run rebase at least once a day.
    ```sh
    git switch main
    git fetch
    git pull -f origin main
    git switch feat/1234-feat-branch
    git rebase main

    # Resolve Conflicts
    # After the rebase is completed
    git push -f origin feat/1234-feat-branch
    ```
9. When the development is finished, Open a pull request to the `main` branch of the original repository.
10. Provide a clear description of your changes and any relevant issue numbers.
11. Solve eventual PR Threads.
12. Merge branch into `main`.

## Testing
- Write unit tests for all new features and bugfixes.
- Use xUnit for testing.
- Place unit tests in the `Unit` folder and integration tests in the `Integration` folder.
- Run all tests before submitting a pull request.
    ```sh
    [command to run tests]
    ```

## Issue Reporting
- Check if the issue has already been reported.
- Provide a clear and descriptive title.
- Include steps to reproduce the issue.
- Describe the expected and actual behavior.
- Provide any relevant screenshots or logs.
