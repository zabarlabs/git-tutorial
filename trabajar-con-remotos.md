## Trabajar con remotos

Una de las potencialidades de Git es poder realizar un trabajo colaborativo, para ello los proyectos suelen estar alojados en algún repositorio en la nube. Los más importantes son GitHub, GitLab o GitBucket. Gestionar un repositorio remoto implica que los usuarios estarán subiendo archivos, trayendo otros a su ordenador local, haciendo modificaciones, etc. Vamos a ver entonces como gestionar este trabajo con remotos.

- **`$ git remote`**: muestra los nombres de los repositorios remotos (deberiamos poder ver al menos `origin` que es el nombre por defecto que Git le ha dado al servidor del que has clonado).
- **`$ git remote -v`**: muestra las URLs que serán usadas tanto para leer como para escribir en ese remoto.

> Un repositorio puede tener múltiples remotos para trabajar con diferentes colaboradores.

### 🚀 Cómo añadir un repositorio remoto

- **`$ git remote add [nombre] [URL]`**: se asocia un remoto a un nombre y a una URL.

```java
$ git remote
origin
$ git remote add zabarlabs https://github.com/zabar/mi-proyecto
$ git remote -v
origin https://github.com/administrador/mi-proyecto (fetch)
origin https://github.com/administrador/mi-proyecto (push)
zabarlabs origin https://github.com/zabar/mi-proyecto (fetch)
zabarlabs origin https://github.com/zabar/mi-proyecto (push)
```

### ↘️ Traer datos desde Remoto

- **`$ git fetch [nombreRemoto]`**: obtenemos los datos del repositorio remoto.

{% hint style='info' %}
`git fetch`solo trae los datos a tu repositorio local, ni lo combina con tu trabajo ni modifica el trabajo que llevas hecho. La combinación con el trabajo se debe hacer manualmente.
{% endhint %}

{% hint style='info' %}
Si clonas un repositorio automaticamente añade ese repositorio remoto con el nombre `origin`
{% endhint %}

- **`$ git pull`**: además de traer los datos del repositorio remoto combina automáticamente la rama remota con la rama actual.

### ↗️ Enviar datos al Remoto

- **`$ git push [nombreRemoto] [nombreRama]`**: envia datos al servidor con nombre y rama especificados.

{% hint style='danger' %}
Este comando solo funciona si ha clonado de un servidor que tienes permiso de escritura y nadie más ha enviado datos de por medio. si alguien ha enviado deberás traerte su trabajo y combinarlo con tuyo antes de poder enviar.
{% endhint %}

### 🔎 Inspeccionar un Remoto

- **`$ git remote show [nombreRemoto]`**: nos da información sobre un remoto en particular y la información sobre el rastreo de ramas.

### ✏️ Eliminar y renombrar Remotos

- **`$ git remote rename [nombreActual] [nuevoNombre]`**: cambia el nombre de una rama.
- **`$ git remote rm [nombreRama]`**: elimina un remoto.
