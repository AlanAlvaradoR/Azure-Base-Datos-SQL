# Azure-Base-Datos-SQL
Creación de base de datos SQL en Azure, lectura y modificacion de datos

![Logo de SQL](https://github.com/AlanAlvaradoR/Azure-Base-Datos-SQL/blob/main/imagenes/SQL.jpg)

## Requisitos

- Cuenta de [Azure](https://portal.azure.com/) con suscripción activa
- Computadora con Windows, Linux o MacOs
- Repositorio DP-900 -> https://github.com/MicrosoftLearning/DP-900T00A-Azure-Data-Fundamentals

---------------------------------------------------------

## Pasos

- Se inicia sesión en la página de [Azure](https://portal.azure.com/)

![Inicio Azure](https://github.com/AlanAlvaradoR/Azure-Base-Datos-SQL/blob/main/imagenes/inicio%20Azure.PNG)

- Se abre el Azure cloud shell por medio del botón mostrado en la siguiente imagen:

![P11-1](https://github.com/AlanAlvaradoR/Azure-Base-Datos-SQL/blob/main/imagenes/P11-1.PNG)

- Se espera a que termine de conectar y se pone el siguiente comando y se da enter:

```Bash
git clone https://github.com/MicrosoftLearning/DP-900T00A-Azure-Data-Fundamentals dp-900
```

![P11-2](https://github.com/AlanAlvaradoR/Azure-Base-Datos-SQL/blob/main/imagenes/P11-2.PNG)

- Se espera a que termine de procesr el comando anterior y se pone el siguiente comando y se da enter:

```Bash
cd dp-900/sql
```

![P11-3](https://github.com/AlanAlvaradoR/Azure-Base-Datos-SQL/blob/main/imagenes/P11-3.PNG)

- Se espera a que termine de procesr el comando anterior y se pone el siguiente comando y se da enter:

```Bash
bash setup.sh
```
*NOTA:* Este último comando pueden tardar varios minutos en completarse, se debe esperar a que termine antes de seguir con el siguiente paso

![P11-4](https://github.com/AlanAlvaradoR/Azure-Base-Datos-SQL/blob/main/imagenes/P11-4.PNG)

- Una vez termine todos los procesos, debería mostrarse de la siguiente forma.

![P11-5](https://github.com/AlanAlvaradoR/Azure-Base-Datos-SQL/blob/main/imagenes/P11-5.PNG)

- Se procede a escribir en el buscador superior de Azure "grupos de recursos" y se selecciona la opción que se muestra en la imagen

![P11-6](https://github.com/AlanAlvaradoR/Azure-Base-Datos-SQL/blob/main/imagenes/P11-6.PNG)

- Se selecciona el último grupo de recursos del lado izquierdo y se desplegará un menú con su contenido en el lado derecho. Se busca el recurso de Base de datos SQL y se da click  en su URL.

![P11-7](https://github.com/AlanAlvaradoR/Azure-Base-Datos-SQL/blob/main/imagenes/P11-7.PNG)

- Se abrirá otra pestaña, se da click en el botón de "Establecer firewall de servidor"

![P11-8](https://github.com/AlanAlvaradoR/Azure-Base-Datos-SQL/blob/main/imagenes/P11-8.PNG)

- Se abrirá otras pestaña, se navega hacia abajo hasta encontrar el apartado de "Reglas de firewall" y se da click en "Agregar la IPv4 del cliente"

![P11-9](https://github.com/AlanAlvaradoR/Azure-Base-Datos-SQL/blob/main/imagenes/P11-9.PNG)

- Se agregará una nueva fila a la lista de firewall, se da click en "guardar".

![P11-10](https://github.com/AlanAlvaradoR/Azure-Base-Datos-SQL/blob/main/imagenes/P11-10.PNG)

- Se regresa al menú del recurso de la base de datos dando click en la siguiente parte:

![P11-11](https://github.com/AlanAlvaradoR/Azure-Base-Datos-SQL/blob/main/imagenes/P11-11.PNG)

- En el menú laterla izquierdo se da click en "Editor de consultas"

![P11-12](https://github.com/AlanAlvaradoR/Azure-Base-Datos-SQL/blob/main/imagenes/P11-12.PNG)

- Nos abrirá una pantalla como la siguiente:

![P11-13](https://github.com/AlanAlvaradoR/Azure-Base-Datos-SQL/blob/main/imagenes/P11-13.PNG)

- Se colocan los siguientes datos para ingresar:

```Bash
login="sampleLogin"
password="samplePassword123!
```

![P11-14](https://github.com/AlanAlvaradoR/Azure-Base-Datos-SQL/blob/main/imagenes/P11-14.PNG)

- Al iniciar sesión se mostrará la siguiente pantalla

![P11-15](https://github.com/AlanAlvaradoR/Azure-Base-Datos-SQL/blob/main/imagenes/P11-15.PNG)

- Escribimos el siguiente comando y damos enter

```SQL
SELECT * FROM Inventory
```

![P11-17](https://github.com/AlanAlvaradoR/Azure-Base-Datos-SQL/blob/main/imagenes/P11-17.PNG)

- Para agregar un nuevo item a "Inventory" escribimos el siguiente comando y damos enter

```SQL
INSERT INTO Inventory(Id, Inventory.NAME, Stock), values(7, 'Strawberry', 500);
```

![P11-19](https://github.com/AlanAlvaradoR/Azure-Base-Datos-SQL/blob/main/imagenes/P11-19.PNG)

- Ahora se escribe el siguiente comando para consultar la base de datos y comprobar que se realizó el cambio:

```SQL
SELECT * FROM Inventory
```



