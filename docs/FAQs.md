## FAQs

Vamos a hacer una página donde podamos responder a una serie de preguntas o plantear el significado de diversos términos que nos ayuden a conocer un poco mejor los entresijos de GIT.

### ✔️ ¿Qué son los Issues de GitHub?

En este apartado de GitHub es donde se recogen los bugs, preguntas e incluso sugerencias para nuevas funcionalidades que los usuarios solicitan a los administradores del proyecto.

### ✔️ ¿Qué es un Pull Request?

Una de la grandes ventajas del desarrollo colaborativo es que podemos hacer un Fork a un proyecto de desarrollo y poder trabajar sobre él. Puede darse el caso que implementos una nueva funcionalidad o resolvamos algún error. En ese caso podemos generar un _Pull Request_ al dueño del proyecto indicandole de esa nueva característica o solución de algún bug y será decisión del propietario si decide incorporarlo al proyecto o no.

### ✔️ ¿Qué es una llave ssh pública?

Permite a cualquier servidor relacionarse con nuestro ordenador sin falta de contraseñas, tanto GitHub como GitLab nos indica que debemos crearla para poder comunicarse con estos repositorios remotos. Podemos crear una llave por cada ordenador desde el que trabajemos, incluso una por usuario de ordenador. Se crean con el siguiente comando desde una carpeta llamada `.ssh` (que está en el directorio del usuario):

```java
ssh-keygen -t rsa
```

La llave generada es un hash bastante largo, debemos copiarlo e introducirlo tanto en GitHub como en GitLab en un apartado localizado en **Setting** llamado _SSH and GPC Keys._
