Quality Analysis Server
====

## :bulb: Definition

According to [Sonarqube Documentation](https://docs.sonarqube.org/latest/)

> SonarQube is a self-managed, automatic code review tool that systematically helps you deliver clean code. As a core element of our Sonar solution, SonarQube integrates into your existing workflow and detects issues in your code to help you perform continuous code inspections of your projects. The tool analyses 30+ different programming languages and integrates into your CI pipeline and DevOps platform to ensure that your code meets high-quality standards.

## :hammer: Sonarcloud

> [clean code in your cloud workflow with {SonarCloud}](https://www.sonarsource.com/products/sonarcloud/.)

### Steps to integrate your project to sonarcloud

Hands on with [Conta Example Project.](https://github.com/persapiens/conta/issues/121)

1. [Login at Sonar Clound with your GitHub account](https://sonarcloud.io/login)

2. Include your organization to analyze using "Plus button" with option "Create new organization"

3. Include your project to analyse using "Plus button" with "Analyse new project" option.

4. Wait first automatic analysis to run. 

5. See your project dashboard inside sonarcloud like [this](https://sonarcloud.io/summary/overall?id=persapiens_conta)


## :construction_worker: Task

Create one pull request for your project according to [Task Submission Guidelines.](../../assessment.md#task-submission)

1. Send a link of your project inside sonarcloud like [this](https://sonarcloud.io/summary/overall?id=persapiens_conta)

2. Configure your project to use an analysis quality server like Sonarcloud. 

3. Fix some issues detected by sonarcloud dashboard of your project like [this](https://github.com/persapiens/conta/issues/121)