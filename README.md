# Red Hat Third-Party Wrapper — Java 21

## 1. Add the vendor JAR

Copy the approved vendor JAR to:

```text
libs/redhat.jar
```

When the filename is different, update `sourceJarName` in `gradle.properties`.

## 2. Configure coordinates

```properties
artifactGroup=com.company.thirdparty
artifactName=redhat
artifactVersion=1.0.0
sourceJarName=redhat.jar
```

## 3. Generate the Gradle wrapper once

```cmd
gradle wrapper --gradle-version 8.10.2
```

Commit all generated wrapper files.

## 4. Build

```cmd
gradlew.bat clean build
```

Expected output:

```text
build/libs/redhat-1.0.0.jar
```

## 5. CloudBees parameters

```text
Java_Version     = Java 21
Gradle_Version   = gradle 8.10.2
JAR_NAME         = redhat
JAR_VERSION      = 1.0.0
GroupID_Name     = com.company.thirdparty
Application_Name = REDHAT_THIRD_PARTY
Service_Name     = redhat-third-party
```

## 6. Consumer dependency

```gradle
implementation "com.company.thirdparty:redhat:1.0.0"
```
