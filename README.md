# spring-boot-security-course

Los antMatchers se ejecutan por orden, es decir si tenemos varios antMatchers se ejecuta el primero, segundo, tercero, etc. por eso es importante el orden.

Lo suyo es poner anotaciones en el Controller y no poner en los antMatchers (@PreAuthorize(""))

Para eso tenemos que añadir la anotación @EnableGlobalMethodSecurity(prePostEnabled = true) en la clase de configuración del
spring security(la clase que extiende de WebSecurityConfigurerAdapter.

csrf -> Cross Site Request Forgery -> es la acción de copiar o imitar una acción, documento, firma.

.csrf().disable() -> esto en produ siempre tiene que estar habilitado.

Lo que hace spring security es generar un CSRF token cuando un usuario se loguea y le devuelve ese token al front y luego el front por cada petición que haga manda ese token, y el back valida que sea el mismo token que le envió cuando el usuario se logueó.

X-XSRF-TOKEN -> esta es la cookie que devuelve el back con el token generado, con el postman podemos verla desde "cookies" y copiar el token y usarlo en otra llamada.

