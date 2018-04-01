# Vuln Dependency Checker

Test `dependency-check`.

https://jeremylong.github.io/DependencyCheck/index.html

## Maven plugin

https://jeremylong.github.io/DependencyCheck/dependency-check-maven/index.html

### How to

#### Run as POM configured plugin

1. Run `mvn verify -DskipTests=true`
1. Open `target/dependency-check-report.html`

#### Run Mojo directly

https://jeremylong.github.io/DependencyCheck/dependency-check-maven/check-mojo.html

1. Run `mvn org.owasp:dependency-check-maven:3.1.1:check --format=ALL -f pom.xml`
1. Open `target/dependency-check-report.html`

##### Issues

Note taking all config properties as command line arguments

## Command line

### How to Run

`dependency-check --project "demo" --scan . --cveUrl12Modified https://nvd.nist.gov/feeds/xml/cve/1.2/nvdcve-modified.xml.gz --cveUrl20Modified=https://nvd.nist.gov/feeds/xml/cve/2.0/nvdcve-2.0-modified.xml.gz --cveUrl12Base=https://nvd.nist.gov/feeds/xml/cve/1.2/nvdcve-%d.xml.gz --cveUrl20Base=https://nvd.nist.gov/feeds/xml/cve/2.0/nvdcve-2.0-%d.xml.gz`

#### Issues

- Not detecting Maven/POM CPEs.

## NSP Analyzer

Only runs online, sending package.json to nsp.
https://github.com/jeremylong/DependencyCheck/blob/master/core/src/main/java/org/owasp/dependencycheck/analyzer/NspAnalyzer.java
https://github.com/jeremylong/DependencyCheck/blob/master/core/src/main/java/org/owasp/dependencycheck/data/nsp/NspSearch.java


# NSP package

https://github.com/nodesecurity/nsp

## How to run offline

1. `npm install -g nsp`
1. `nsp gather` - downloads advisories for offline checking
1. `nsp check --offline --advisories advisories.json`
