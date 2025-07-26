# 📚 LiterAlura Challenge - Java

Este proyecto es parte del desafío propuesto por Alura LATAM, el cual consiste en desarrollar una aplicación Java que consuma la API pública de libros [Gutendex](https://gutendex.com/), almacene información relevante en una base de datos PostgreSQL y permita consultar distintos datos sobre libros y autores desde una interfaz de consola.

---

## 🚀 Tecnologías utilizadas

- Java 17
- Spring Boot 3
- Spring Web
- Spring Data JPA
- PostgreSQL
- Lombok
- Jackson (para procesar JSON)
- Maven

---

## 🎯 Funcionalidades

✅ Importar libros desde la API de Gutendex\
✅ Almacenar libros y autores en una base de datos\
✅ Consultar libros por idioma\
✅ Consultar autores vivos después de cierta fecha\
✅ Listar los 10 libros más descargados\
✅ Interfaz en consola simple e interactiva

---

## 🧱 Estructura del proyecto

```
src/
├── main/
│   ├── java/com/literalura/
│   │   ├── model/          # Entidades JPA: Book, Author
│   │   ├── repository/     # Interfaces JPA
│   │   ├── service/        # Lógica de negocio y consumo de API
│   │   ├── dto/            # Clases para mapear respuesta de la API
│   │   └── AppRunner.java  # Lógica de consola con menú interactivo
│   └── resources/
│       └── application.properties
```

---

## ⚙️ Configuración

1. Asegúrate de tener PostgreSQL instalado y ejecutando.
2. Crea una base de datos:

```sql
CREATE DATABASE literalura_db;
```

3. Configura el archivo `application.properties`:

```properties
spring.datasource.url=jdbc:postgresql://localhost:5432/literalura_db
spring.datasource.username=tu_usuario
spring.datasource.password=tu_contraseña
spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
```

---

## 🛠 Cómo ejecutar

1. Clona el repositorio:

```bash
git clone https://github.com/tu_usuario/literalura-challenge-java.git
cd literalura-challenge-java
```

2. Compila el proyecto y ejecútelo:

```bash
./mvnw spring-boot:run
```

3. Interactúa con el menú en consola.

---

## 📡 Sobre la API Gutendex

Este proyecto utiliza [https://gutendex.com/books/](https://gutendex.com/books/) para obtener información pública de libros del Proyecto Gutenberg.

La estructura JSON se mapea mediante clases DTO y luego se transforma en entidades para su almacenamiento.

---

## ✍️ Autor

Roberto Antonio Alferes Gómez\
💼 Proyecto educativo basado en el challenge de [Alura Latam](https://www.aluracursos.com/)

---

## 📝 Licencia

Este proyecto está bajo la licencia MIT. Libre de usar con fines educativos y personales.

