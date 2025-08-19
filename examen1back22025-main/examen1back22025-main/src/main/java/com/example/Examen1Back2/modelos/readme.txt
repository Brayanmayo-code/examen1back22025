CURSO.JAVA =
En esta carpeta los cambios que hice fueron:

estaba mal escrito la anotacion de @I y es @Id

estaba mal copiado el @GeneratedValue(strategy = GenerationType.IDENTITY)
estaba copiado de esta manera @Ge(strategy = IDENTITY)

Al  private String nombre le faltaba ;

la anotacion @JoinColumn no lleva ; al final

Faltaba private a la linea Docente docente y el ;

Y faltaba el metodo constructor


DOCENTE.JAVA =
En esta carpeta los cambios que hice fueron:

Estaba mal escrito la anotacion @Entity estaba de esta manera @Entit

Falbataba el @id en la linea 10 arriba de la linea id

faltaba el constructor vacio y el constructor lleno

faltaban los getters y setters para cursos y usuarios solo habia para id y especialidad


USUARIOS.JAVA =
En esta carpeta estabal mal copiado el @Entity estaba de esta manera @Entit

en la linea 10 la  faltaba terminar de copiarlo le faltaba el IDENTITY

El el @column estaba mal escrito estaba de esta manera @Colun

Faltaban los gueters y setters para los atributos
Y el construtor

CONEXION A LA BASE DE DATOS =
La conexion a la base de datos la hago en application.properties
primero lo organizo porque estaba de esta manera = spring.application.name=Examen1Back2
                                                   BASE DATOS ACA
Para ponerlo de esta manera = spring.application.name=banck2-Desempeño
                              spring.datasource.url=jdbc:mysql://localhost:8012/develop_db
                              spring.datasource.username=root
                              spring.datasource.password=
                              spring.jpa.hibernate.ddl-auto=update
profe dependiendo el localhost  el numero de la terminal de xampp se conecta la base de datos en este caso en mi computador es 8012

url: le dice a Spring dónde está la base de datos (localhost, puerto 3306).

username: tu usuario de MySQL (normalmente es root).

password: la clave del usuario MySQL como en este caso no tengo lo dejo vacio

ddl-auto=update: significa que Spring crea o actualiza las tablas automáticamente según las clases.

show-sql=true: muestra en la consola los comandos SQL que se están ejecutando



Documentacion con IA generativa =
6) Recomendaciones para evitar errores futuros

Convenciones Java: evitar caracteres especiales en nombres de variables/campos (usar contrasena).

Anotaciones JPA: validar la ortografía (@Entity, @Id, @GeneratedValue, @Column, etc.).

Relaciones bidireccionales: definir claramente lado propietario (@JoinColumn) y lado inverso (mappedBy).

Serialización JSON: en relaciones bidireccionales usar @JsonManagedReference / @JsonBackReference o @JsonIgnore donde aplique.

Migraciones: en proyectos reales usar herramientas como Flyway o Liquibase en lugar de ddl-auto=update.

Validación: agregar @Column(nullable = false, length = ...) y @Enumerated(EnumType.STRING) para enums.

Pruebas rápidas: al compilar, revisar el log de Hibernate para detectar nombres de tabla/columna y relaciones.

Commits atómicos: un cambio por commit, mensaje claro y en presente.

7) (Opcional) Enum de tipos de usuario

Archivo sugerido: TipoUsuario.java

