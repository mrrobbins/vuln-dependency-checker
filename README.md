# Vuln Dependency Checker

Test `dependency-check`.

https://jeremylong.github.io/DependencyCheck/index.html

# Maven plugin

https://jeremylong.github.io/DependencyCheck/dependency-check-maven/index.html

## How to

### Run as POM configured plugin

1. Run `mvn verify -DskipTests=true`
1. Open `target/dependency-check-report.html`

### Run Mojo directly

https://jeremylong.github.io/DependencyCheck/dependency-check-maven/check-mojo.html

1. Run `mvn org.owasp:dependency-check-maven:3.1.1:check`
1. Open `target/dependency-check-report.html`
