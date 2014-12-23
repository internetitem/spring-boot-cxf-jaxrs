Spring Boot CXF Integration
===========================

Spring Boot integration for CXF, specifically for JAX-RS.

## Usage ##

Add the following to your `pom.xml` (updating `<version>` where appropriate):

    <dependency>
        <groupId>com.internetitem.spring</groupId>
        <artifactId>spring-boot-cxf-jaxrs</artifactId>
        <version>1.0</version>
    </dependency>

Then, add the following to a `@Configuration` class:

    @Import(com.internetitem.spring.cxf.CxfConfiguration.class)

Now, all beans tagged with `@Path` will be automatically added as JAX-RS Services. All beans tagged with `@Provider` will be added as JAX-RS Providers.

## Dependencies ##

You must declare Spring, Spring Boot and CXF as dependencies. This POM will bring in Jackson (for JSON support) automatically.

## Customization ##

 * The property `cxf.path` can be used to customize where the CXF Servlet is "mounted". It defaults to "`/services/*`"
 * If the property `cxf.log.requests` is set, request data will be logged
 * If a bean returning the type `JacksonJaxbJsonProvider` is found, that will be used instead of the built-in version
 * If a bean returning the type `ObjectMapper` is found, that will be used instead of the built-in version

