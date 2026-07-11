# Contributing to paykit-go

First off, thank you for considering contributing to **paykit-go**! 🎉

Our goal is to build a production-ready Go SDK that provides a unified interface for integrating African payment providers such as M-Pesa, Airtel Money, and Pesapal. Every contribution—whether it's code, documentation, bug reports, or feature suggestions—is appreciated.

## Getting Started

### 1. Fork the Repository

Fork the repository to your GitHub account and clone it locally.

```bash
git clone https://github.com/<your-username>/paykit-go.git
cd paykit-go
```

Add the upstream repository:

```bash
git remote add upstream https://github.com/Flying-Tea-Squad/paykit-go.git
```

### 2. Create a Branch

Create a new branch from `main`.

```bash
git checkout -b feat/my-feature
```

Branch naming examples:

* `feat/stk-push`
* `fix/token-cache`
* `docs/update-readme`
* `test/mpesa-client`

## Development Setup

Ensure you have:

* Go 1.24 or later
* Git

Download dependencies:

```bash
go mod tidy
```

Run formatting:

```bash
go fmt ./...
```

Run tests:

```bash
go test ./...
```

## Project Structure

```
paykit-go/
├── gateway/          # Provider registry
├── bogus/            # Test gateway implementation
├── mpesa/            # M-Pesa provider
├── airtelmoney/      # Airtel Money provider
├── pesapal/          # Pesapal provider
├── callback/         # Shared callback utilities
├── driver/           # Import all providers
└── docs/             # Project documentation
```

Each provider should be self-contained and implement the shared gateway interfaces defined by the root package.

## Coding Guidelines

* Follow standard Go formatting (`go fmt`).
* Write clear, idiomatic Go code.
* Keep functions small and focused.
* Avoid unnecessary abstractions.
* Prefer composition over inheritance.
* Add comments for exported types and functions.

## Testing

Every new feature or bug fix should include tests whenever practical.

Run all tests before submitting a pull request:

```bash
go test ./...
```

Fixtures for provider responses should be placed inside each provider's `fixtures/` directory.

## Commit Messages

This project follows the Conventional Commits specification.

Examples:

```
feat(mpesa): add OAuth token caching
fix(callback): validate callback signature
docs: update contributing guide
test(mpesa): add stk push fixtures
refactor(http): simplify retry logic
chore: initialize project structure
```

## Pull Requests

Before opening a Pull Request, make sure:

* Your branch is up to date with `main`.
* Your code is formatted.
* All tests pass.
* New functionality includes tests where appropriate.
* Documentation has been updated if necessary.

Your Pull Request should include:

* A short description of the change.
* The motivation behind it.
* Screenshots or logs if applicable.
* A reference to the related issue (e.g. `Closes #12`).

## Reporting Issues

When opening an issue, please include:

* A clear description of the problem.
* Steps to reproduce.
* Expected behavior.
* Actual behavior.
* Go version.
* Operating system.

## Adding a New Payment Provider

Each provider should:

* Live in its own package.
* Implement the shared gateway interface.
* Handle provider-specific authentication internally.
* Normalize responses into the common `Response` type.
* Include fixtures and tests.
* Document any provider-specific configuration.

## Code of Conduct

Please be respectful and constructive in all interactions. We welcome contributors of all experience levels and strive to maintain a friendly, collaborative environment.

Happy coding! 🚀
# Contributing to paykit-go

First off, thank you for considering contributing to **paykit-go**! 🎉

Our goal is to build a production-ready Go SDK that provides a unified interface for integrating African payment providers such as M-Pesa, Airtel Money, and Pesapal. Every contribution—whether it's code, documentation, bug reports, or feature suggestions—is appreciated.

## Getting Started

### 1. Fork the Repository

Fork the repository to your GitHub account and clone it locally.

```bash
git clone https://github.com/<your-username>/paykit-go.git
cd paykit-go
```

Add the upstream repository:

```bash
git remote add upstream https://github.com/Flying-Tea-Squad/paykit-go.git
```

### 2. Create a Branch

Create a new branch from `main`.

```bash
git checkout -b feat/my-feature
```

Branch naming examples:

* `feat/stk-push`
* `fix/token-cache`
* `docs/update-readme`
* `test/mpesa-client`

## Development Setup

Ensure you have:

* Go 1.24 or later
* Git

Download dependencies:

```bash
go mod tidy
```

Run formatting:

```bash
go fmt ./...
```

Run tests:

```bash
go test ./...
```

## Project Structure

```
paykit-go/
├── gateway/          # Provider registry
├── bogus/            # Test gateway implementation
├── mpesa/            # M-Pesa provider
├── airtelmoney/      # Airtel Money provider
├── pesapal/          # Pesapal provider
├── callback/         # Shared callback utilities
├── driver/           # Import all providers
└── docs/             # Project documentation
```

Each provider should be self-contained and implement the shared gateway interfaces defined by the root package.

## Coding Guidelines

* Follow standard Go formatting (`go fmt`).
* Write clear, idiomatic Go code.
* Keep functions small and focused.
* Avoid unnecessary abstractions.
* Prefer composition over inheritance.
* Add comments for exported types and functions.

## Testing

Every new feature or bug fix should include tests whenever practical.

Run all tests before submitting a pull request:

```bash
go test ./...
```

Fixtures for provider responses should be placed inside each provider's `fixtures/` directory.

## Commit Messages

This project follows the Conventional Commits specification.

Examples:

```
feat(mpesa): add OAuth token caching
fix(callback): validate callback signature
docs: update contributing guide
test(mpesa): add stk push fixtures
refactor(http): simplify retry logic
chore: initialize project structure
```

## Pull Requests

Before opening a Pull Request, make sure:

* Your branch is up to date with `main`.
* Your code is formatted.
* All tests pass.
* New functionality includes tests where appropriate.
* Documentation has been updated if necessary.

Your Pull Request should include:

* A short description of the change.
* The motivation behind it.
* Screenshots or logs if applicable.
* A reference to the related issue (e.g. `Closes #12`).

## Reporting Issues

When opening an issue, please include:

* A clear description of the problem.
* Steps to reproduce.
* Expected behavior.
* Actual behavior.
* Go version.
* Operating system.

## Adding a New Payment Provider

Each provider should:

* Live in its own package.
* Implement the shared gateway interface.
* Handle provider-specific authentication internally.
* Normalize responses into the common `Response` type.
* Include fixtures and tests.
* Document any provider-specific configuration.

## Code of Conduct

Please be respectful and constructive in all interactions. We welcome contributors of all experience levels and strive to maintain a friendly, collaborative environment.

Happy coding! 🚀
