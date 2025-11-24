# JDK Import in Maven Projects in IDEA

## Introduction
This test plan defines the strategy and approach for testing the correctness of IntelliJ IDEA’s import of the Java language level in Maven-based projects.

## General Information
Project name: "JDK Import in Maven Projects in IDEA"<br>
Testing purpose: To verify how correctly IntelliJ IDEA imports the Java language level in Maven-based projects.<br>
Testing date: 24.11.2025

## Description of the Test Cases
Single-module Maven project:
- Java version set via `<properties>` `<maven.compiler.source>` and `<maven.compiler.target>`
- Java version level set via `<properties>` `<maven.compiler.release>`
- Java version level set via `<plugin>` `<source>` and `<target>`
- Java version level set via `<plugin>` `<release>`

Multi-module Maven project (inheritance):
- Java version inheritance via `<properties>` `<maven.compiler.source>` and `<maven.compiler.target>`
- Java version inheritance via `<properties>` `<maven.compiler.release>`
- Java version inheritance via `<plugin>` `<source>` and `<target>`
- Java version inheritance via `<plugin>` `<release>`

Multi-module Maven project (override):
- Java version override: parent via `<properties>` `<maven.compiler.source>` and `<maven.compiler.target>`, child via `<properties>` `<maven.compiler.release>`
- Java version override: parent via `<properties>` `<maven.compiler.release>`, child via `<plugin>` `<source>` and `<target>`
- Java version override: parent via `<plugin>` `<source>` and `<target>`, child via `<properties>` `<maven.compiler.release>`
- Java version override: parent via `<plugin>` `<release>`, child via `<properties>` `<maven.compiler.source>` and `<maven.compiler.target>`

Multi-module Maven project (toolchain):
- Java version set via `toolchains.xml`

## Criteria for Test Completion
All test cases have been successfully completed, and no critical defects have been found. All critical defects have been fixed and retested, testing completed as planned.

## Test Environment
IntelliJ IDEA 2025.2.2 (Community Edition)<br>
Apache Maven 3.9.11<br>
Java version: 24.0.2

## Responsible Parties
Tester: Ekaterina Kiricheva<br>
Project Manager: Sofia Kondirova

## Conclusion
The test plan has been developed and approved by all stakeholders. Testing of the Java language level import in Maven projects in IntelliJ IDEA will be conducted according to the described test cases.