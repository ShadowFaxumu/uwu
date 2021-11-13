# PIA - 3VIL TOOL

**_3VIL TOOL_** es un programa que contiene herramientras para realizar tareas con relación a ciberseguridad.
Entre ellas están:
* [Envio de correos](https://github.com/S4yago/pia-pc/blob/main/envio_de_correos.py)
* [Consulta a la API de GitHub](https://github.com/S4yago/pia-pc/blob/main/api_github.py)
* [Escaneo de puertos](https://github.com/S4yago/pia-pc/blob/main/port_scanning.py)
* [Obtención de claves HASH](https://github.com/S4yago/pia-pc/blob/main/claves_hash.py)
* [Cifrado de texto](https://github.com/S4yago/pia-pc/blob/main/cifrado_de_texto.py)

## Comenzando 🚀

### Pre-requisitos

Para poder tener una ejecución exitosa del script se necesitaran instalar ciertos modulos 
que no vengan por default en python. Para ello ejecutará el siguiente comando

```
$ pip install -r requirements.txt
```
## Funcionamiento general

### Envio de correos

La herramienta de envio de correos, se utiliza para que puedas enviar correos electrónicos con dominio _gmail_, 
a una o más personas con la posibilidad de adjuntar archivos. El script, trabaja con 3 archivos dados por el usuario  que son:

* Un archivo .json - Que debe contener la información de la cuenta remitente, con esta estructura:

```
{
  "user": "su correo electrónico"
  "pass: "su contraseña"
  }
```

* Un archivo .txt - Que debe contener la información a enviar en el email, con esta estructura:

--> En la primera linea deberán estar todos los correos, a los que les quieras mandar el email, separadas por una coma  
--> En la segunda linea deberá intrucir el asunto(que no deberá ser más de una línea)  
--> Y de la cuarta linea en adelante podrá introducir todo el cuerpo de su email  

Por ejemplo:
```
correo1@gmail.com,correo2@gamil.com,correo3@gmail.com
Este es mi asunto

Este es el cuerpo
de mi 
email c:
```

* El path absoluto donde se encuentra el archivo que desea adjuntar

Por ejemplo:

```
C:\Users\Documentos\Imagenes\Imagen3.png
```

### Cifrado de texto

La herramienta de cifrado de texto utiliza dos métodos (Cesar y Transposición) para codificar, decodificar y crackear un texto dado en formato .txt, tiene
la función, para que en tiempo de ejecución, se devuelva el texto ya codificado con el método y llaves indicadas.  
Para la función de crackeo también se cuenta con la posibilidad de indicar el idioma en el que se desea crackear un mensaje donde se podrá escoger entre
Inglés y Español (en, es)
El script trabaja con 1 archivo dado por el usuario:

* Path absoluto del txt

Por ejemplo:
```
C:\Users\Documentos\Archivo.txt
```

### Obtención de claves HASH

### Consulta a la API de GitHub

### Escaneo de puertos

## Ejecución

El script principal es **3v1l_tool.py**, que tiene 2 métodos:
* Con paso de argumentos
* Por menú

### Con paso de argumentos

Para poder diferenciar entre alguna herramienta y otra se tomará en cuenta el parámetro **_'-m'_**  
Donde las opciones son: 
* _email_ - para envio de correos
* _encoding_ - para cifrado de texto
* _hash_ - para obtención de claves HASH
* _api_ - para consulta a la API de GitHub

Por ejemplo:

```
$ 3vil_tool.py -m email
```

Para ejecutar la herramienta de **Envio de correos**, se tomarán en cuenta los parametros:

* -json - Que será el path del archivo .json
* -txt - Que será el path del archivo .txt
* -file - Que será el path del archivo a adjuntar

Por ejemplo:

```
$ 3vil_tool.py -m email --email -json "path del .json" --email -txt "path del .txt" --email file "path del archivo"
```
## Autores ✒️

_Con la contribución de:_

* [Gómez Rodriguez Paulina](https://github.com/ShadowFaxumu) -Cifrado de texto- y -Envio de correos-
* [Sayago Leiba Angel Saul](https://github.com/S4yago) -Consulta a la API de GITHUB-
* [Rodriguez Rangel Deivi](https://github.com/LicYoshio) -Obtención de claves HASH-
* [Gaytan Montelongo Jesus Gerardo](https://github.com/Moncho96) -Escaneo de puertos-
