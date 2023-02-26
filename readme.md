## **Instalacion de dependencias**

+ **[--save-dev]** o **[-D]**: guardar como dependencia que solamente sera utilizada en el entorno de desarollo y nunca sera llevada a produccion.

+ **[--save]** o **[-S]**: guardar dependencia para ser llevada a produccion.

+ **Paquetes globales [-g]** : ligados a nuesro OS
<br>


## **Instalacion de dependencias de versiones especificas**

+ **[-o]** : Instalar de forma opcional una dependencia

+ **[--dry-run]** : Esto simulara una instalacion (sin agregarlo al proyecto) y si no tiene conflictos, se pueden agregar

+ **[npm install ______@version]** : Instala una dependencia en la version que nosotros especifiquemos

+ **[npm install ______@latest]** : Actualiza la dependencia a la ultima version que haya
<br>


## **Comandos de NPM (Scripts)** ##

Para crear un comando en tu proyecto, utiliza la siguiente estructura, donde es el nombre del comando que debería ser muy descriptivo y es el comando que utilizarías en la terminal.

```json
	... { 
		"scripts": { 
			"<nombre>": "<comando>" 
		} 
	}
```

Una vez hayas escrito el comando en el archivo package.json, la manera de ejecutarlo en la terminal será con el comando npm run <nombre>.

+ **[npx]**: ejecutar acciones particulares sin necesidad de pasar por la instalacion, o sea que si nosotros queremos hacer un proyecto nuevo. [npx] [accion] [argumento]

<br>


## **Actualización de dependencias** ##

+ **[npm update]** : Para actualizar todas las dependencias.


+ **[npm outdate]** : muestra una tabla con las versiones de todas las dependencias instaladas.

**UNMET DEPENDECY :** dependencia no instalada, cuando haces el npm install, se instala la ultima version.

A veces tendremos que actualizar en pares las dependencias para que no haya conflicto.
<br>


## **Seguridad y solución de problemas**

al instalar una dependencia nos puede salir una linea de vulnerabilidades (moderado, alto, critico)

+ **[npm audit]**: nos brinda informacion para tomar desicion de que va a pasar

+ **[npm audit --json]**: nos brinda informacion mas detallada en forma de un objeto 

+ **[npm audit fix]**: procede a actualizar los recursos necesarios para que no tengamos vulnerabilidades, nos entrega un recurso que nos muestra que elementos quedan

+ **[npm audit fix --force]**: intentar de todo para poder evitar las vulnerabilidades

si con el fix --force sigue habiendo vulnerabilidades, podemos probar actualizar los paquetes a la version mas reciente o que el audit fix --force nos diga que actualizemos