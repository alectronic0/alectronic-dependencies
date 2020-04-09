# Alectronic Dependencies

A BOM (Bill of Material) contains Springboot and Spring Clouds dependency manager along with some 3rd party libaries.

## Getting Started

in your root `build.gradle`
````groovy
    dependencyManagement {
        imports {
            mavenBom "co.alectronic:alectronic-dependencies:${alectronicDependenciesVersion}"
        }
    }
````
in your `gradle.properties`
````properties
alectronicDependenciesVersion=1.0.0.+
````

## Dependencies
Below is a list of all dependencies with version within this BOM.

### Other Dependencies Managers
| Group ID | Artifact ID | Version Name | Version | Note |
| --- | --- | --- | --- | --- |
| `org.springframework.boot` | `spring-boot-dependencies` |`${springBootDependenciesVersion}`| 2.2.2.RELEASE  | https://docs.spring.io/spring-boot/docs/2.2.2.RELEASE/reference/html/appendix-dependency-versions.html |
| `org.springframework.cloud` | `spring-cloud-dependencies` | `${springCloudDependenciesVersion}` | Greenwich.RELEASE | |

### 3rdPartyLibraries
| Group ID | Artifact ID | Version Name | Version | Note |
| --- | --- | --- | --- | --- |
| `org.apache.commons` | `commons-email` | `${apacheCommonsEmailVersion}` | 1.5 |
| `org.apache.commons` | `commons-text` | `${apacheCommonsTextVersion}` | 1.6 |
| `commons-io` | `commons-io` | `${apacheCommonsIoVersion}` | 2.6 |
| `au.com.dius` | `pact-jvm-consumer-junit_2.12` | `${pactJvmVersion}` | 3.5.25 |
| `io.rest-assured` | `rest-assured` | `${restAssuredVersion}` | 4.0.0 |
| `io.springfox` | `springfox-swagger-ui` | `${swaggerVersion}` | 2.9.2 |
| `io.springfox` | `springfox-swagger2` | `${swaggerVersion}` | 2.9.2 |
| `com.github.tomakehurst` | `wiremock-jre8` | `${wiremockVersion}` | 2.23.2 |

## Contributing
###### Owners
Alec Doran-Twyford

###### Rules
* If you adjust a version please update this within the readme & update the changelog and bump version.
  * Major for any Major or Minor Dependencies update.
  * Minor for any Major Libraries changes or Patch Dependencies updates.
  * Patch for any Minor Libraries changes.
  * SNAPSHOT for any Patch Libraries changes.

###### Note
