## Trabajar con remotos

Una de las potencialidades de Git es poder realizar un trabajo colaborativo, para ello los proyectos suelen estar alojados en algún repositorio en la nube. Los más importantes son GitHub, GitLab o GitBucket. Gestionar un repositorio remoto implica que los usuarios estarán subiendo archivos, trayendo otros a su ordenador local, haciendo modificaciones, etc. Vamos a ver entonces como gestionar este trabajo con remotos.

- **`$ git remote`**: muestra los nombres de los repositorios remotos (deberiamos poder ver al menos `origin` que es el nombre por defecto que Git le ha dado al servidor del que has clonado).
- **`$ git remote -v`**: muestra las URLs que serán usadas tanto para leer como para escribir en ese remoto.

### 🚀 Cómo añadir un repositorio remoto

- **`$ git remote add [nombre] [URL]`**: se asocia un remoto a un nombre y a una URL.

{% hint style="info" %}
La URL se coge de la barra de direcciones del navegador que muestra la dirección del repositoro remoto que queremos añadir.  
{% endhint %}

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

{% hint style='info' %}
Si clonas un repositorio, automaticamente la referencia a ese remoto se llamará `origin`
{% endhint %}

{% hint style='tip' %}  
Un repositorio puede tener múltiples remotos para trabajar con diferentes colaboradores.  
{% endhint %}

### ↘️ Traer datos desde Remoto

- **`$ git fetch [nombreRemoto]`**: obtenemos los datos del repositorio remoto.

{% hint style='info' %}
`git fetch`solo trae los datos a tu repositorio local, ni los combina con tu trabajo ni modifica el trabajo que llevas hecho. La combinación con tu trabajo se hará manualmente.
{% endhint %}

- **`$ git pull [nombreRemoto] [nombreRama]`**: además de traer los datos del repositorio remoto combina automáticamente la rama remota con la rama actual.

### ↗️ Enviar datos al Remoto

- **`$ git push [nombreRemoto] [nombreRama]`**: envia datos al servidor con nombre y rama especificados.

{% hint style='danger' %}
Este comando solo funciona si se ha clonado de un servidor en el que tienes permiso de escritura y nadie más ha enviado datos de por medio. Si alguien ha enviado datos, deberás traerte su trabajo y combinarlo con el tuyo antes de poder enviar.
{% endhint %}

### 🔎 Inspeccionar un Remoto

- **`$ git remote show [nombreRemoto]`**: nos da información sobre un remoto en particular y la información sobre el rastreo de ramas.

### ✏️ Eliminar y renombrar Remotos

- **`$ git remote rename [nombreActual] [nuevoNombre]`**: cambia el nombre de una rama.
- **`$ git remote rm [nombreRama]`**: elimina un remoto.
