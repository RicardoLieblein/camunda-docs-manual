---

title: 'Supported Environments'
weight: 40

menu:
  main:
    identifier: "user-guide-introduction-supported-environments"
    parent: "user-guide-introduction"

---


Run the Camunda Platform in every Java-runnable environment. Camunda Platform is supported with our QA infrastructure in the following environments. Here you can find more information about our [enterprise support](http://camunda.com/bpm/enterprise/).

{{< note title="Supported Environments" class="info" >}}
  Please note that the environments listed in this section depend on the version of the Camunda Platform. Please select the corresponding version of this documentation to see the environment that fits to your version of the Camunda Platform. e.g., [supported environments for version 7.15](http://docs.camunda.org/7.15/guides/user-guide/#introduction-supported-environments)
{{< /note >}}


# Container/Application Server for Runtime Components

## Application-Embedded Process Engine

* All Java application servers
* Camunda Spring Boot Starter: Embedded Tomcat (see [Supported versions]({{< ref "/user-guide/spring-boot-integration/version-compatibility.md" >}}) and [Deployment scenarios]({{< ref "/user-guide/spring-boot-integration/_index.md#supported-deployment-scenarios" >}}))

## Container-Managed Process Engine and Camunda Cockpit, Tasklist, Admin

* Apache Tomcat 9.0
* JBoss EAP 7.0 / 7.1 / 7.2 / 7.3
* Wildfly Application Server 13.0 / 14.0 / 15.0 / 16.0 / 17.0 / 18.0 / 19.0 / 20.0 / 21.0 / 22.0 / 23.0
* IBM WebSphere Application Server 8.5 / 9.0 ([Enterprise Edition only](http://camunda.com/enterprise/))
* Oracle WebLogic Server 12c (12R2) ([Enterprise Edition only](http://camunda.com/enterprise/))


# Databases

## Supported Database Products

* MySQL 5.7 / 8.0
* MariaDB 10.2 / 10.3
* Oracle 12c / 19c
* IBM DB2 11.1 (excluding IBM z/OS for all versions)
* PostgreSQL 9.6 / 10 / 11 / 12 / 13
* Amazon Aurora PostgreSQL compatible with PostgreSQL 9.6 / 10.4 / 10.7 / 10.13 / 12.4
* Microsoft SQL Server 2014/2016/2017/2019 (see [Configuration Note]({{< ref "/user-guide/process-engine/database/mssql-configuration.md" >}}))
* H2 1.4 (not recommended for [Cluster Mode]({{< ref "/introduction/architecture.md#clustering-model" >}}) - see [Deployment Note]({{< ref "/user-guide/process-engine/deployments.md" >}}))
* CockroachDB v20.1.3 (see [Configuration guide]({{< ref "/user-guide/process-engine/database/cockroachdb-configuration.md" >}}) for more details)

## Database Clustering & Replication

Clustered or replicated databases are supported given the following conditions. The communication between Camunda Platform and the database cluster has to match with the corresponding non-clustered / non-replicated configuration. It is especially important that the configuration of the database cluster guarantees the equivalent behavior of READ-COMMITTED isolation level.

* MariaDB Galera Cluster: Galera Cluster for MariaDB is supported with specific configuration settings and some known limitations. See [Details]({{< ref "/user-guide/process-engine/database/mariadb-galera-configuration.md" >}}).

# Web Browser

* Google Chrome latest
* Mozilla Firefox latest
* Microsoft Edge latest


# Java

* Java 8 / 9 / 10 / 11 / 12 / 13 / 14 (if supported by your application server/container)


# Java Runtime

* Oracle JDK 8 / 9 / 10 / 11 / 12 / 13 / 14
* IBM JDK 8 (with J9 JVM)
* OpenJDK 8 / 9 / 10 / 11 / 12 / 13 / 14, including builds of the following products:
  * Oracle OpenJDK
  * AdoptOpenJDK (with HotSpot JVM)
  * Amazon Corretto
  * Azul Zulu

# Camunda Modeler

Supported on the following platforms:

* Windows 7 / 10
* Mac OS X 10.11
* Ubuntu LTS (latest)

Reported to work on

* Ubuntu 12.04 and newer
* Fedora 21
* Debian 8

# Maintenance Policy

Check our [Enterprise Announcements page](/enterprise/announcement/) for confirmed changes to our supported environments in upcoming releases.

## Adding Environments

Whenever a new version of one of the following environments is released, we target support of that new version with the next minor release of Camunda Platform:

* Java Language
* Wildfly Application Server
* Oracle Database

The exact release in which we support a new environment depends on factors such as the release date of the environment and the required implementation effort.

Version support for other environments is decided case by case, much of which is based on the demand in our user base.

## Removing Environments

Whenever a new version of one of the following environments is supported, we usually discontinue support of the oldest version with the same release:

* Wildfly Application Server

Note that we may decide to deviate from this policy on a case-by-case basis.
