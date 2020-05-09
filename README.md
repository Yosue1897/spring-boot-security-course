# spring-boot-security-course

Los antMatchers se ejecutan por orden, es decir si tenemos varios antMatchers se ejecuta el primero, segundo, tercero, etc. por eso es importante el orden.

Lo suyo es poner anotaciones en el Controller y no poner en los antMatchers (@PreAuthorize(""))

Para eso tenemos que añadir la anotación @EnableGlobalMethodSecurity(prePostEnabled = true) en la clase de configuración del
spring security(la clase que extiende de WebSecurityConfigurerAdapter.
