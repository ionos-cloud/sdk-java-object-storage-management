[![Gitter](https://img.shields.io/gitter/room/ionos-cloud/sdk-general)](https://gitter.im/ionos-cloud/sdk-general)
[![Maven Central](https://maven-badges.herokuapp.com/maven-central/com.ionoscloud/ionos-cloud-sdk/badge.svg?style=plastic)](https://mvnrepository.com/artifact/com.ionoscloud/ionos-cloud-sdk)

## Overview

Object Storage Management API is a RESTful API that manages the object storage
service configuration for IONOS Cloud.


## Getting Started

### Installation

To install the API client library to your local Maven repository, simply execute:

```shell
mvn clean install
```

To deploy it to a remote Maven repository instead, configure the settings of the repository and execute:

```shell
mvn clean deploy
```

Refer to the [OSSRH Guide](http://central.sonatype.org/pages/ossrh-guide.html) for more information.

#### Maven users

Add this dependency to your project's POM:

```xml
<dependency>
  <groupId>com.ionoscloud.objectstoragemanagement</groupId>
  <artifactId>ionos-cloud-sdk-object-storage-management</artifactId>
  <version>1.0.0</version>
  <scope>compile</scope>
</dependency>
```

#### Gradle users

Add this dependency to your project's build file:

```groovy
compile "com.ionoscloud.objectstoragemanagement:ionos-cloud-sdk-object-storage-management:1.0.0"
```

#### Others

At first generate the JAR by executing:

```shell
mvn clean package
```

Then manually install the following JARs:

* `target/ionos-cloud-sdk-object-storage-management-1.0.0.jar`
* `target/lib/*.jar`

## Feature Reference

The ionos-cloud-sdk-object-storage-management SDK for JAVA aims to offer access to all resources in the IONOS Container Registry API and also offers some additional features that make the integration easier:
 - authentication for API calls
 - handling of asynchronous requests

## Authentication

All available server URLs are:

- *https://s3.ionos.com* - Production

By default, *https://s3.ionos.com* is used, however this can be overriden at authentication by changing
the `basePath` in the default client.

The username and password or the authentication token can be manually specified when initializing
the sdk client:

```java
// Import classes:
import com.ionoscloud.objectstoragemanagement.ApiClient;
import com.ionoscloud.objectstoragemanagement.ApiException;
import com.ionoscloud.objectstoragemanagement.ApiResponse;
import com.ionoscloud.objectstoragemanagement.Configuration;
import com.ionoscloud.objectstoragemanagement.auth.*;
import com.ionoscloud.objectstoragemanagement.model.*;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();

    // Configure HTTP bearer token authorization:
    HttpBearerAuth tokenAuthentication = (HttpBearerAuth) defaultClient.getAuthentication("tokenAuth");
    tokenAuthentication.setBearerToken("IONOS_TOKEN");

    // OR
    // defaultClient.setBearerToken("IONOS_TOKEN");

    // Configure API URL
    defaultClient.setBasePath("IONOS_API_URL");
  }
}

```

## FAQ

 - How can I open a bug/feature request?
	Bugs & feature requests can be open on the repository issues: https://github.com/ionos-cloud/com.ionoscloud.objectstoragemanagement/issues/new/choose

 - Can I contribute to the Java SDK?
    Pur SDKs are automatically generated using OpenAPI Generator and don’t support manual changes. If you need changes please open an issue and we’ll try to take care of it.
