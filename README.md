# ¿Qué es Git?

Git es lo que se conoce como un control de versiones y actua como un backup de los cambios que vayamos haciendo en nuestro proyecto (ya sea de desarrollo o escribir un libro por ejemplo).  
Lo realmente potente de esta herramienta es que nos permite volver a un estado anterior de nuestro proyecto con relativa facilidad, además todos los cambios que vayamos generando estarán documentados lo que nos permite en todo momento saber lo que estamos haciendo.

{% hint style='info' %}
El creador de Git es el mismo que el de Linux, Linus Torvals
{% endhint %}

Desde la pagina de **[Git](https://git-scm.com/)** podemos descargar el instalador para Windows, que incluye una terminal de comandos llamada **Git Bash**.

## ¿Qué es un repositorio?

Un repositorio es una carpeta donde tendremos alojado nuestro proyecto. Para que este sea un repositorio Git tendrá que contener una carpeta oculta llamada **`.git`**. Los cambios que vayamos haciendo se irán guardando en esta carpeta.  
Para inicializar un repositorio se utiliza el comando:  
**`$ git init`**  
A partir de ese momento los archivos que se incluyan en el repositorio serán continuamente rastreados por Git y cual cambio o modificación quedará registrado.

## Configuración inicial

Git permite obtener y establecer una serie de variables de configuración que controlan el aspecto y el funcionamiento de Git. Esto lo podemos controlar mediante el comando **`git config`**.

Vamos a ver que configuraciones podemos hacer:

- **`$ git config --global user.name "Mi Nombre"`**: establece el nombre de usuario.
- **`$ git config --global user.email miNombre@ejemplo.com`**: establece el email.
- **`$ git config --global core.editor Code`**: establece VS Code como editor por defecto.
- **`$ git config --list`**: lista las propiedades que Git ha configurado.

## ¿Cómo se obtiene ayuda?

Saberse todos los comandos que tiene Git además de ser muy complicado, no es muy práctico. Git nos provee de un manual donde nos explica que es lo que hace cada comando, tenemos varias formas de acceder al mismo:

```java
$ git help <comando>
$ git <comando> --help
```
