# Solución Taller: Volúmenes y Bind Mounts en Docker (Linux/macOS)

**Autor:** Cristian Javier Gómez Pérez  
**Código:** 202310427  

---

## Ejercicio 1 — Bind mount en modo lectura con Nginx

**Pasos:**

1. Crear carpeta y archivo y Levante Nginx con bind mount de solo lectura.

![Pasos 1 y 2](Recursos-Ejercicio1/Pasos1-2.png)

2. Abra http://localhost:8080 y verifique. 

![Paso 3](Recursos-Ejercicio1/Paso3.png)

3. Edite index.html en el host y recargue el navegador, el cambio debe verse. 

![Paso 4_1](Recursos-Ejercicio1/Paso4_1.png)

![Paso 4_2](Recursos-Ejercicio1/Paso4_2.png)

4. Intente crear un archivo dentro del contenedor.

![Paso 5](Recursos-Ejercicio1/Paso5.png)


## Ejercicio 2 - Named volume con PostgreSQL

**Pasos:**

1. Cree un volumen.

![Paso 1](Recursos-Ejercicio2/Paso1.png)

2. Ejecute PostgreSQL.

![Paso 2](Recursos-Ejercicio2/Paso2.png)

3. Cree una tabla y agregue datos.

![Paso 3](Recursos-Ejercicio2/Paso3.png)

4. Elimine el contenedor.

![Paso 4](Recursos-Ejercicio2/Paso4.png)

5. Vuelva a levantarlo usando el mismo volumen y verifique que los datos siguen allí.

![Paso 5](Recursos-Ejercicio2/Paso5.png)


## Ejercicio 3 - Volumen compartido entre dos contenedores

**Pasos:**

1. Cree un volumen.

![Paso 1](Recursos-Ejercicio3/Paso1.png)

2. Productor (escribe timestamps cada segundo).

![Paso 2](Recursos-Ejercicio3/Paso2.png)

3. Consumidor (lee en tiempo real).

![Paso 3](Recursos-Ejercicio3/Paso3.png)

4. Reinicie el productor y revise que el archivo siga creciendo.

![Paso 4](Recursos-Ejercicio3/Paso4.png)


## Ejercicio 4 — Backup y restauración de un volumen

**Pasos:**

1. Cree un volumen y añade un archivo.

![Paso 1](Recursos-Ejercicio4/Paso1.png)

2. Haga backup a un tar en el host.

![Paso 2](Recursos-Ejercicio4/Paso2.png)

3. Restaure en un nuevo volumen.

![Paso 3](Recursos-Ejercicio4/Paso3.png)

4. Verifique el contenido restaurado.

![Paso 4](Recursos-Ejercicio4/Paso4.png)


## Reflexion:
- Durante el desarrollo del taller pude reforzar conceptos clave sobre cómo los contenedores manejan la persistencia de datos y cómo se comunican con el sistema host, adicionalmente aprendí que los volúmenes son la clave para mantener datos persistentes. Los problemas que tuve fueron principalmente de sintaxis en Bash (saltos de línea con \, redirecciones, y separación de comandos), pero al entender cómo funciona el shell pude resolverlos.