Coding Standards
====

## :bulb: Definition

According to [Wikipedia](https://en.wikipedia.org/wiki/Coding_conventions)

> Coding conventions are a set of guidelines for a specific programming language that recommend programming style, practices, and methods for each aspect of a program written in that language. These conventions usually cover file organization, indentation, comments, declarations, statements, white space, naming conventions, programming practices, programming principles, programming rules of thumb, architectural best practices, etc.


## :hammer: Spring Java Format

[Spring Java Format](https://github.com/spring-io/spring-javaformat) is a set of plugins that can be applied to any Java project to provide a consistent “Spring” style. The set currently consists of: 

- A source formatter that applies wrapping and whitespace conventions.

- A checkstyle plugin that enforces consistency across a codebase.


## :hammer: Checkstyle

[Checkstyle is a development tool to help programmers write Java code that adheres to a coding standard. It automates the process of checking Java code to spare humans of this boring (but important) task. This makes it ideal for projects that want to enforce a coding standard.](https://checkstyle.sourceforge.io/)

### Install and Run with Visual Code

Use [VSCode Spring Format for Java](https://github.com/spring-io/spring-javaformat?tab=readme-ov-file#visual-studio-code)

Hands on with [Conta Example Project:](https://github.com/persapiens/conta/issues/166) format and verify.

### Install and Run with Maven

Use [spring-javaformat-maven-plugin](https://github.com/spring-io/spring-javaformat?tab=readme-ov-file#maven)

Hands on with [Conta Example Project:](https://github.com/persapiens/conta/issues/166) format and verify.

## :construction_worker: Task

Create one pull request for your project according to [Task Submission Guidelines.](../../assessment.md#task-submission)

Install one coding standard tool like Spring Java Format in your project.

Fix coding standard issues reported by the coding standard tool. 

Create a separate commit to each type of fixed coding standard.

Include coding standard check in your build pipeline.
