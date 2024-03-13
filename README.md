<h1>Instancia EC2 a AWS desde Terraform</h1>
Suponiendo que tendrás cuenta de AWS que permita credenciales, terraform y AWS CLI instalado, haremos lo siguiente:
<br/>
<h2> 1. Creación de un usuario IAM </h2>
<img src="img/tf/img1.png" alt="Texto alternativo">
<br/>
Nos dirigimos hacia "usuarios".
<img src="img/tf/img2.png" alt="Texto alternativo">
<br/>
Luego, crear usuario y le asignamos un nombre.
<img src="img/tf/img3.png" alt="Texto alternativo">
<br/>
Presionamos aquí
<img src="img/tf/img4.png" alt="Texto alternativo">
<br/>
Luego, AdministratorAcces 
<img src="img/tf/img5.png" alt="Texto alternativo">
<br/>
Creamos el usuario
<img src="img/tf/img6.png" alt="Texto alternativo">
<br/>
Vemos, como se creo correctamente y nos dirigimos a el
<img src="img/tf/img7.png" alt="Texto alternativo">
<br/>
Necesitamos las credenciales, así que presionamos en "Credenciales de Seguridad"
<img src="img/tf/img8.png" alt="Texto alternativo">
<br/>
Presionamos en "Crear clave de acceso"
<img src="img/tf/img9.png" alt="Texto alternativo">
<br/>
Siguiente, en CLI y la creamos, es opcional la etiqueta de descripción
<img src="img/tf/img10.png" alt="Texto alternativo">
<img src="img/tf/img11.png" alt="Texto alternativo">
<br/>
Aquí tenemos a las claves de acceso, las guardamos en un notepad
<img src="img/tf/img12.png" alt="Texto alternativo">
<img src="img/tf/img13.png" alt="Texto alternativo">
<br/>
<br/>
<h2> 2. Accesos </h2>
Creamos una carpeta donde queremos que este nuestro proyecto, lo abrimos en visual estudio code, abrimos una terminal y escribimos **aws configure** y cargamos las claves que creamos en el paso anterior
<img src="img/tf/img14.png" alt="Texto alternativo">
<br/>
Luego, en el editor creamos un archivo **main.tf** y copiamos lo siguiente:
<img src="img/tf/img15.png" alt="Texto alternativo">
<br/>
Guardamos, y volvemos a la terminal donde escribiremos **terraform init**, este comando lo que hace es inicializar el directorio, se descargaran e instalaran todos los proveedores definidos en la configuracion
<img src="img/tf/img16.png" alt="Texto alternativo">
<br/>
Luego, con **terraform apply** creamos la infraestructura. Lo que devuelve es largo, en **Enter a value: yes** 
<img src="img/tf/img17.png" alt="Texto alternativo">
<img src="img/tf/img18.png" alt="Texto alternativo">
<br/>
Para este momento ya hemos creado la instancia EC2, si vamos a AWS la podremos visualizar
<img src="img/tf/img19.png" alt="Texto alternativo">
<br/>
Podemos inspeccionar el estado con **terraform show**
<img src="img/tf/img20.png" alt="Texto alternativo">
<br/>
También, existe la gestión manueal del estado con **terraform state list**
<img src="img/tf/img21.png" alt="Texto alternativo">
<br/>


