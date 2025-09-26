# SXE_tarea02
## Pasos a seguir
### 1. Crea un repositorio en GitHub
Creamos en Github un repositorio para esta tarea, con Readme incluido para poder dar la explicación sobre la instalación del WordPress.  

<img width="500" height="400" alt="imagen" src="https://github.com/user-attachments/assets/99c7f0c8-afe6-43b3-b298-3c359522df3f" />

### 2. Instala Ubuntu Server en una máquina virtual
En mi caso, yo tengo el Ubuntu normal 

<img width="600" height="450" alt="imagen" src="https://github.com/user-attachments/assets/1787b4e8-742b-4dcc-bd8b-248f5ce33c58" />  

### 3. Guía para instalar WordPress en Ubuntu Server  

Una vez en la máquina virtual, tenemos que actualizar todo con un sudo apt update.

<img width="600" height="450" alt="Captura desde 2025-09-25 14-23-36" src="https://github.com/user-attachments/assets/36419d80-3e0b-4e3e-9ab3-d1dd8356d579" /> 

Luego instalamos PHP y Apache con el siguiente comando. sudo apt install apache2 \
                 ghostscript \
                 libapache2-mod-php \
                 mysql-server \
                 php \
                 php-bcmath \
                 php-curl \
                 php-imagick \
                 php-intl \
                 php-json \
                 php-mbstring \
                 php-mysql \
                 php-xml \
                 php-zip

<img width="600" height="450" alt="Captura desde 2025-09-25 14-25-07" src="https://github.com/user-attachments/assets/30b875e4-d334-407d-8b75-6c2949a1743e" />  

Ahora procedemos a crear el directorio de instalación y descargar el archivo de WordPress.org:  

<img width="600" height="450" alt="Captura desde 2025-09-25 14-27-30" src="https://github.com/user-attachments/assets/45bf5360-c6b6-4c2e-95d1-2fae24895ecf" />  

#### 3.1 Configuración de Apache para Wordpress

Creamos un archivo en Apache para que muestre WordPress desde su carpeta y funcione correctamente. /etc/apache2/sites-available/wordpress.conf con un "sudo nano..." y posteriormente pegaremos el contenido de la imagen, y finalmente terminaremos guardándolo con un "ctrl + s".  

<img width="600" height="450" alt="Captura desde 2025-09-25 14-33-26" src="https://github.com/user-attachments/assets/ca1c1842-aa9e-4663-935b-c9c5dcadc9bf" />  

Habilitamos el archivo con "sudo a2ensite wordpress"
Activa la reescritura de URL con: sudo a2enmod rewrite
Desactivar el sitio predeterminado de "Funciona" con: sudo a2dissite 000-default 
Finalmente, recarga apache2 para aplicar todos estos cambios:  sudo service apache2 reload  

<img width="600" height="450" alt="imagen" src="https://github.com/user-attachments/assets/925167e0-024d-4881-aa83-d7d2c74c854c" />

<img width="944" height="534" alt="Captura desde 2025-09-26 13-01-54" src="https://github.com/user-attachments/assets/b0308d73-6cce-4c63-8247-4f2aeaa90f8b" />

<img width="946" height="252" alt="Captura desde 2025-09-26 13-02-19" src="https://github.com/user-attachments/assets/5362e4f1-a316-4433-8721-a8834e747815" />
<img width="944" height="257" alt="Captura desde 2025-09-26 13-02-50" src="https://github.com/user-attachments/assets/6aa52062-016a-46fd-8c07-bd3378a40d7b" />
<img width="932" height="309" alt="imagen" src="https://github.com/user-attachments/assets/893327ae-4655-4c13-b45a-803a8b3f6835" />
Finalmente lo habilitamos con sudo service mysql start


