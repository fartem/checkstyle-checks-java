# checkstyle-checks-java

[![GitHubActions](https://github.com/fartem/checkstyle-checks-java/workflows/Build/badge.svg)](https://github.com/fartem/checkstyle-checks-java/actions?query=workflow%3ABuild)

## About

Custom Checkstyle checks for Java projects.

## Checks

| Check                                 | Description                                        |
|---------------------------------------|----------------------------------------------------|
| `UtilityClassPrivateConstructorCheck` | Check primary private constructor in Utility class |

## Installation

### Gradle

Add `https://jitpack.io` as Maven repository to `build.gradle` (needs for downloading dependencies from GitHub):

```groovy
repositories {
    maven {
        url "https://jitpack.io"
    }
}
```

If you are using [Checkstyle plugin](https://docs.gradle.org/current/userguide/checkstyle_plugin.html) for Gradle, add
checks project as dependency in the `dependencies` section in the `build.gradle`:

```groovy
checkstyle 'com.github.fartem:checkstyle-checks-java:master'
```

## How to use

Add to `TreeWalker` module:

```xml

<module name="com.smlnskgmail.jaman.checkstyle.checks.UtilityClassPrivateConstructorCheck">
    <property name="id" value="UtilityClassPrivateConstructorCheck"/>
</module>
```

## How to contribute

Read [Commit Convention](https://github.com/fartem/repository-rules/blob/master/commit-convention/COMMIT_CONVENTION.md).
Make sure your build is green before you contribute your pull request. Then:

```shell
./gradlew clean
./gradlew build
```

If you don't see any error messages, submit your pull request.

## Contributors

- [@fartem](https://github.com/fartem) as Artem Fomchenkov
