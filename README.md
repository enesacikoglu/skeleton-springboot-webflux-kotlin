# webflux playground

Note: this is just quick and dirty playground

- https://speakerdeck.com/sdeleuze/functional-web-applications-with-kotlin-and-spring-5
- https://www.infoq.com/articles/reactor-by-example


## findings
- springfox swagger currently does not work with webflux, since it has dependencies to mvc

    Caused by: java.lang.NoClassDefFoundError: org/springframework/web/servlet/mvc/method/annotation/RequestMappingHandlerAdapter
    	at springfox.documentation.spring.web.ObjectMapperConfigurer.postProcessBeforeInitialization(ObjectMapperConfigurer.java:45) ~[springfox-spring-web-2.6.1.jar:2.6.1]
    	
    	it requires: import org.springframework.web.servlet.mvc.method.annotation.RequestMappingHandlerAdapter;
    	
    	
 todo: try to include mvc, but factory spring boot with webflux ????
    	
- I created a feature request: https://github.com/springfox/springfox/issues/1809    	
    	
## gradle modules

- common: some shared code (example)
- rest-service-classic: (reactive) mvc-style restcontroller example
- rest-service: (reactive) functional-style router example

## project flavours

This project has been implemented in different flavours:

### kotlin
- spring boot 1.5.* & spring-mvc: https://github.com/bastman/skeleton-springboot-kotlin 
- spring boot 2.0.* & spring-webflux: https://github.com/bastman/skeleton-springboot-webflux-kotlin

### java
- spring boot 1.5.* & spring-mvc: https://github.com/bastman/skeleton-springboot-java 