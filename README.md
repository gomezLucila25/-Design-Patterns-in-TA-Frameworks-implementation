# Design Patterns in Test Automation Frameworks

> **Module 3 of my EPAM Test Automation track.** Each module added one layer to the same Selenium framework.
> The complete, final version lives in **[selenium-framework-patterns](https://github.com/gomezLucila25/selenium-framework-patterns)**.

## What this module added

- The framework was refactored around **SOLID** principles. Every pattern documents the problem it solves:
  - **Factory Method**: one `WebDriverCreator` per browser, with no `switch` statement (OCP);
  - **thread-safe Singleton**: `ConfigProvider` with double-checked locking;
  - **Singleton + ThreadLocal**: `DriverManager`, for parallel runs;
  - **Decorator**: logging and element highlighting around actions, with the driver injected (DIP);
  - **Strategy**: swappable wait strategies (explicit vs fluent).
- **Allure** reporting with `@Feature`, `@Story` and `@Step` and screenshots on failure (see `jenkins-screenshots/allure`).

## Stack

Java 17 · Selenium 4 · TestNG · Allure · AssertJ · Log4j2 · Maven · Jenkins

## Run

```bash
mvn clean test
```
