Spring Boot CXF Integration
===========================

Spring Boot integration for CXF, specifically for JAX-RS.

## Usage ##

    @Import(com.internetitem.spring.cxf.CxfConfiguration.class)

All beans tagged with `@Path` will be added as JAX-RS Services. All beans tagged with `@Provider` will be added as JAX-RS Providers.

## Dependencies ##

You must declare Spring, Spring Boot and CXF as dependencies. This POM will bring in Jackson (for JSON support) automatically.

## Customization ##

 * The property `cxf.path` can be used to customize where the CXF Servlet is "mounted". It defaults to "`/services/*`"
 * If the property `cxf.log.requests` is set, request data will be logged
 * If a bean returning the type `JacksonJaxbJsonProvider` is found, that will be used instead of the built-in version
 * If a bean returning the type `ObjectMapper` is found, that will be used instead of the built-in version

