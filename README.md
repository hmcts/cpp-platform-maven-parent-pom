# cpp-platform-maven-parent-pom

`uk.gov.moj.cpp.common:parent-pom`

The root Maven parent POM for the Criminal Practice Platform (CPP). It mirrors the role of `cp-maven-parent-pom` in the framework tier but serves the platform and bounded-context tier: `cpp-platform-libraries`, `cpp-platform-core-domain`, `cpp-platform-maven-service-parent-pom`, and all `cpp-context-*` services inherit from this project (directly or transitively).

## Position in the hierarchy

```
maven-super-pom  (external)
└── cpp-platform-maven-parent-pom  ← this project
    ├── cpp-platform-maven-common-bom
    └── cpp-platform-libraries
        └── cpp-platform-maven-service-parent-pom
            └── [all cpp-context-* bounded-context services]
```

`cp-maven-parent-pom` is a sibling — both inherit from `maven-super-pom` independently.

## Maven coordinates

| Property | Value |
|---|---|
| `groupId` | `uk.gov.moj.cpp.common` |
| `artifactId` | `parent-pom` |
| Parent | `uk.gov.justice:maven-super-pom` |

## What this POM provides

**Java / Jakarta EE target**
- Java 21 (`<compiler.source/target/release>21`)
- Jakarta EE 10
- Enforcer requires Java ≥ 21 and Maven ≥ 3.3.9

**Build conventions** (same as the framework tier)
- Compiler warnings and lint enabled; max 100 errors / 100 warnings
- `src/raml/json` copied to `target/generated-test-resources/json`
- `src/raml/json/schema` copied to `target/generated-resources/json/schema`
- JaCoCo coverage agent wired to all test phases
- `ci.buildNode` populated from environment on Windows and Unix
- `web.context.root` defaults to `/${project.artifactId}` (overridable per WAR)

**Plugin management** — same plugin stack as `cp-maven-parent-pom`: compiler, surefire/failsafe, enforcer, jacoco, jar, war, resources, assembly, source, javadoc, buildnumber, versions, pitest, sonar, wildfly, liquibase, exec.

**Profiles** — `raml-jar`, `liquibase-jar`, `jandex-index`, `release`, `pitest`, `windows`/`unix`.

**Enforcer rules** — in addition to the standard Java/Maven version checks, this POM includes `enforce-moj-latest-interfaces` which verifies that dependencies on MOJ interface JARs (such as `progression-query-api`) reference the latest released version. This rule has `<skip>false</skip>` hardcoded and cannot be bypassed with `-Denforcer.skip=true`.
