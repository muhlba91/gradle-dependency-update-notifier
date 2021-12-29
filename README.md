# Dependency Update Notifier (Gradle Plugin)

[![Build Status](https://img.shields.io/github/workflow/status/muhlba91/gradle-dependency-update-notifier/Release?style=for-the-badge)](https://github.com/muhlba91/gradle-dependency-update-notifier/actions)
[![Gradle Plugin Portal](https://img.shields.io/maven-metadata/v/https/plugins.gradle.org/m2/org/muehlbachler/gradle/plugin/dependency-update-notifier/org.muehlbachler.gradle.plugin.dependency-update-notifier.gradle.plugin/maven-metadata.xml.svg?label=Gradle%20Plugin&style=for-the-badge)](https://plugins.gradle.org/plugin/org.muehlbachler.gradle.plugin.dependency-update-notifier)
[![Release Date](https://img.shields.io/github/release-date/muhlba91/gradle-dependency-update-notifier?style=for-the-badge)](https://github.com/muhlba91/gradle-dependency-update-notifier/releases)
[![Documentation](https://img.shields.io/badge/docs-latest-yellow.svg?style=for-the-badge)](https://muhlba91.github.io/gradle-dependency-update-notifier)
[![CPAN](https://img.shields.io/cpan/l/Config-Augeas.svg?style=for-the-badge)](https://github.com/muhlba91/gradle-dependency-update-notifier/blob/master/LICENSE)
[![Sonarcloud Status](https://sonarcloud.io/api/project_badges/measure?project=org.muehlbachler.gradle.plugin.dependency-update-notifier&metric=alert_status)](https://sonarcloud.io/dashboard?id=org.muehlbachler.gradle.plugin.dependency-update-notifier)
[![Sonarcloud Status](https://sonarcloud.io/api/project_badges/measure?project=org.muehlbachler.gradle.plugin.dependency-update-notifier&metric=security_rating)](https://sonarcloud.io/component_measures/metric/security_rating/list?id=org.muehlbachler.gradle.plugin.dependency-update-notifier)
[![SonarCloud Coverage](https://sonarcloud.io/api/project_badges/measure?project=org.muehlbachler.gradle.plugin.dependency-update-notifier&metric=coverage)](https://sonarcloud.io/component_measures/metric/coverage/list?id=org.muehlbachler.gradle.plugin.dependency-update-notifier)
[![SonarCloud Bugs](https://sonarcloud.io/api/project_badges/measure?project=org.muehlbachler.gradle.plugin.dependency-update-notifier&metric=bugs)](https://sonarcloud.io/component_measures/metric/reliability_rating/list?id=org.muehlbachler.gradle.plugin.dependency-update-notifier)
[![SonarCloud Vulnerabilities](https://sonarcloud.io/api/project_badges/measure?project=org.muehlbachler.gradle.plugin.dependency-update-notifier&metric=vulnerabilities)](https://sonarcloud.io/component_measures/metric/security_rating/list?id=org.muehlbachler.gradle.plugin.dependency-update-notifier)
[![Known Vulnerabilities](https://snyk.io/test/github/muhlba91/gradle-dependency-update-notifier/badge.svg?targetFile=build.gradle)](https://snyk.io/test/github/muhlba91/gradle-dependency-update-notifier?targetFile=build.gradle)
<a href="https://www.buymeacoffee.com/muhlba91" target="_blank"><img src="https://cdn.buymeacoffee.com/buttons/default-orange.png" alt="Buy Me A Coffee" height="28" width="150"></a>

This Gradle plugin creates GitLab issues for outdated project dependencies found by the [Gradle Versions Plugin](https://github.com/ben-manes/gradle-versions-plugin).

Link to the [Gradle Plugin Registry](https://plugins.gradle.org/plugin/org.muehlbachler.gradle.plugin.dependency-update-notifier).

---

## Documentation

The documentation can be found [here](https://muhlba91.github.io/gradle-dependency-update-notifier).

---

## Usage

### `plugins` block:

Build script snippet for plugins DSL for Gradle 2.1 and later:

```groovy
plugins {
  id "org.muehlbachler.gradle.plugin.dependency-update-notifier" version "$version"
}
```

### `buildscript` block:

Build script snippet for use in older Gradle versions or where dynamic configuration is required:

```groovy
apply plugin: "org.muehlbachler.gradle.plugin.dependency-update-notifier"

buildscript {
  repositories {
    maven { url "https://plugins.gradle.org/m2/"}
  }

  dependencies {
    classpath "org.muehlbachler.gradle.plugin.dependency-update-notifier:$version"
  }
}
```

### GitLab Issue Notifier

After configuring the plugin and executing `dependencyUpdates` from the *Versions plugin*, you can run

```
gradle gitlabDependencyUpdateNotifier
```

to create an issue like:

![Created Issue](docs/images/issue.png)

---

### Commit Message

This project follows [Conventional Commits](https://www.conventionalcommits.org/), and your commit message must also
adhere to the additional rules outlined in `.conform.yaml`.

---

## Release

To draft a release, use [standard-version](https://github.com/conventional-changelog/standard-version):

```bash
$ standard-version
# alternatively
$ npx standard-version
```

Finally, push with tags:

```bash
$ git push --follow-tags
```

---

## Contributions

Please feel free to contribute, be it with Issues or Pull Requests! Please read
the [Contribution guidelines](CONTRIBUTING.md)

## Supporting

If you enjoy the application and want to support my efforts, please feel free to buy me a coffe. :)

<a href="https://www.buymeacoffee.com/muhlba91" target="_blank"><img src="https://cdn.buymeacoffee.com/buttons/default-orange.png" alt="Buy Me A Coffee" height="75" width="300"></a>
