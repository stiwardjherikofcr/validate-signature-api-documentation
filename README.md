# API -Signature Recognition

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

## Descripción Y Contexto
Esta API esta construido en el lenguaje Python usando las tecnologias de Django REST Framework

## Requirements
- Python 3.9.10
- Django 4.0.2
- Django REST Framework 3.13.1
- Tensorflow 2.8.0

### Nota
Descarga el [modelo](https://drive.google.com/file/d/1-2abDVQcrRF9CUYRqTMIVXn5f_DGUizW/view?usp=sharing).

## Instalación
Primero, clone el repositorio en su máquina local:
```bash
git clone https://github.com/Sachica/validate_signature.git
```

Después de clonar el repositorio, desea crear un entorno virtual, por lo que tiene una instalación de python limpia.
Puedes hacer esto ejecutando el comando:
```
python -m venv venv
```

Después de esto, es necesario activar el entorno virtual, puede obtener más información al respecto [Aqui](https://docs.python.org/3/tutorial/venv.html)
```
venv\Scripts\activate
```

Luego instalar todas las dependencias requeridas ejecutando el comando:
```
pip install -r requirements.txt
```

## Ejecutar el Proyecto localmente
Finalmente, ejecute el servidor de desarrollo:
```bash
python manage.py runserver
```

El proyecto estará disponible en **127.0.0.1:8000/signature-recognition/**

## Estructura
En una API RESTful, los puntos finales (URL) definen la estructura de la API y cómo los usuarios finales acceden a los datos de nuestra aplicación utilizando los métodos HTTP: GET, POST, PUT, DELETE.

En nuestro caso, tenemos un solo recurso, `signature-recognition`, por lo que usaremos las siguientes URL: `/signature-recognition/` para imagenes en base64, respectivamente:

Endpoint |HTTP Method | CRUD Method | Result
-- | -- |-- |--
`signature-recognition` | POST | READ | Determina si la imagen corresponde a una Firma (SI=1) ó (NO=0)

## POST

Request Link
 ```
  --- /signature-recognition/
   ```
 Request Body
 ```  
  {
  "image": "Aca va la imagen en base64"
  }
  ```
 Response Body
 
 ```
{
    "class_label": 1,
    "confidence": 98.23856949806213
}
```

## Autor(es)

**David Fernando Rojas Sáchica - Desarrollador**

-   <https://github.com/Sachica>
 
**Manuel Alejandro Coronel Andrade - Desarrollador**

-   <https://github.com/ManuelCoronelAndrade>
   
**Stiward Jherikof Carrillo Ramírez - Desarrollador**

-   <https://github.com/stiwardjherikofcr>

## Institución Académica

**[Programa de Ingeniería de Sistemas]** de la **[Universidad Francisco de Paula Santander]**

[Programa de Ingeniería de Sistemas]: https://ingsistemas.cloud.ufps.edu.co/
[Universidad Francisco de Paula Santander]: https://ww2.ufps.edu.co/

## Licencia
El código fuente se publica bajo la [MIT License](https://github.com/sibtc/django-multiple-user-types-example/blob/master/LICENSE).