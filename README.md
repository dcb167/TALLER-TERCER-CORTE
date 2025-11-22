# TALLER TERCER CORTE

## Elaborado por: Laura Rodriguez y Diana Bernal

### 1. Simulación de los Robots de Softbank Robotics 

+ A continuación, es posible evidenciar el proceso para desarrollar la simulación de los robots de softbank robotics del respositorio denominado: "Humanoid Gym" y su respectivo despliegue en Docker:

![Imagen de WhatsApp 2025-11-21 a las 14 25 29_c1125374](https://github.com/user-attachments/assets/06130f7e-c4cd-4341-9c73-af84e3aed1e5)</br>

<strong>Figura 1.</strong> Crear un nuevo directorio en Ubuntu.

![Imagen de WhatsApp 2025-11-21 a las 14 25 30_dbec4334](https://github.com/user-attachments/assets/e3a90039-17c6-4652-b374-761a7faecc06)</br>

<strong>Figura 2.</strong> Actualización de los paquetes.

![Imagen de WhatsApp 2025-11-21 a las 14 25 30_6b9fa262](https://github.com/user-attachments/assets/09a83d8a-f359-4336-a9a8-6182c0749d53)</br>

<strong>Figura 3.</strong> Crear un nuevo entorno virtual.

![Imagen de WhatsApp 2025-11-21 a las 14 25 30_5f9418ea](https://github.com/user-attachments/assets/dc3452dc-47b5-4fe7-ab62-a8908ee4272f)</br>

<strong>Figura 4.</strong> Instalación de las respectivas dependencias.

![Imagen de WhatsApp 2025-11-21 a las 14 25 30_986382e3](https://github.com/user-attachments/assets/3737d642-3e07-4684-819c-7ce321f5b6c0)</br>

<strong>Figura 5.</strong> Instalación de la librería pybullet en Ubuntu.

![Imagen de WhatsApp 2025-11-21 a las 14 25 30_5e769b8f](https://github.com/user-attachments/assets/d7363135-a3c0-4d50-b93f-c9a478d13817)</br>

<strong>Figura 6.</strong> Accediendo al respectivo directorio.

![Imagen de WhatsApp 2025-11-21 a las 14 25 31_94008d90](https://github.com/user-attachments/assets/776e108b-c1ed-4c5d-a8d3-97dd4358a687)</br>

<strong>Figura 7.</strong> Crear los respectivos archivos para la Visualización de los Robots.

![Imagen de WhatsApp 2025-11-21 a las 14 25 31_3ae34434](https://github.com/user-attachments/assets/511c82fc-75ca-426d-81b0-9b2bcae4b3aa)</br>

<strong>Figura 8.</strong> Visualización de la Implementación en Python (1).

![Imagen de WhatsApp 2025-11-21 a las 14 25 31_480bec3b](https://github.com/user-attachments/assets/a3d72b13-2598-4910-ae17-11cebdc2be15)</br>

<strong>Figura 9.</strong> Visualización de la Simulación de Dancer.

![Imagen de WhatsApp 2025-11-21 a las 14 25 31_871b9ab3](https://github.com/user-attachments/assets/ca7f15c4-fba6-483d-86fc-f8b5ba82f8d6)</br>

<strong>Figura 10.</strong> Visualización de la Simulación de Nao.

![Imagen de WhatsApp 2025-11-21 a las 14 25 31_58400a26](https://github.com/user-attachments/assets/a5ea7d3b-59ca-4037-83b3-aabe0a6c4532)</br>

<strong>Figura 11.</strong> Visualización de la Simulación de Romeo.

![Imagen de WhatsApp 2025-11-21 a las 14 25 32_e223d60d](https://github.com/user-attachments/assets/55f19d93-fe92-4eb6-9afa-bb17062d8c9e)</br>

<strong>Figura 12.</strong> Visualización de la Simulación de Pepper.

## 3. Búsqueda conceptual y despliegue

### 3.1 Búsqueda conceptual (Kubernete)

##### ¿Que es Kubernete?
En palabras mas senceillas Kebernete es una plataforma de orquestación de contenedores diseñada para automatizar:
+ El despliegue
+ La gestión
+ La escalabilidad
+ La recuperación ante fallos
de aplicaciónes empaquetadas de contenedores.

Fue creado por Google y hoy es mantenido por la Cloud Native Computing Foundation (CNCF).

##### Caracteristicas;

1. Alta disponibilidad (High Availability):
El clúster se replica y se auto-recupera cuando un nodo falla.

2. Escalabilidad automática (Auto-Scaling):
Aumenta o reduce la cantidad de Pods dependiendo de la demanda.

3. Auto-reparación (Self-Healing):
Si un contenedor falla, Kubernetes lo reemplaza automáticamente.

4. Balanceo de carga:
Distribuye tráfico entre Pods para garantizar rendimiento.

5. Automatización en el despliegue:
Permite hacer rolling updates y rollbacks.

6. Observabilidad:
Incluye monitoreo, registros y métricas integradas.

7. Desacoplamiento del hardware
Funciona en nubes públicas, privadas o infraestructura local.

##### Arquitectura general:

###### Master Node (Control Plane):
Coordina el clúster en cual incluye:

+ API Server: Puerta de entrada al clúster
+ Scheduler: Decide dónde ejecutar Pods
+ Controller Manager: Tareas automáticas del sistema
+ etcd: Base de datos distribuida de estado del clúster

###### Worker Nodes
Cada nodo ejecuta contenedores y contiene:

+ Kubelet: Agente que controla los Pods
+ Kube-Proxy: Red interna y balanceo
+ Runtime de contenedores: Docker, containerd, CRI-O

###### Objetos clave dentro del clúster:

+ Pod: Unidad más pequeña: contiene uno o varios contenedores
+ Deployment: Gestiona replicas, actualizaciones y rollback
+ Service: Expone Pod(s) dentro o fuera del clúster
+ Namespace: Aislamiento lógico dentro del clúster
+ ConfigMap/Secret: Configuración externa y variables

##### Aplicaciones de Kubernetes:

+ Ejecución de microservicios
+ Aplicaciones escalables a demanda
+ Sistemas distribuidos
+ Plataformas empresariales de alta disponibilidad
+ CI/CD (Continuous Integration / Deployment)
+ Procesamiento de datos y machine learning

##### Relación entre Kubernetes y los contenedores:
Kubernetes no crea contenedores, sino que los orquesta.

+ Docker: crea y ejecuta contenedores.
+ Kubernetes: gestiona miles de contenedores en clusters.

Kubernetes usa contenedores (Docker, containerd o CRI-O) como unidades de ejecución, pero agrega capacidades que Docker solo no tiene

### ITEM 2: Contenedores
##### ¿Que es Docker?
Docker es una plataforma para empaquetar, distribuir, ejecutar aplicaciones dentro de contenedores, los cuales son unidades ligeras, portables y aisladas.
###### Conceptos claves de Docker:

+ Imagen: Es una plantilla: contiene el sistema base y la aplicación.

+ Contenedor: Instancia ejecutable creada a partir de una imagen.

+ Dockerfile: Archivo de instrucciones para crear una imagen.

+ Registry: Repositorio de imágenes (ej: Docker Hub).

##### ¿Como crear contenedores?

1. Primero se inicia con la instalación de Docker usando los siguientes comandos, incluidos los de autorizar permisos:

+ sudo apt update
+ sudo apt install docker.io -y
+ sudo systemctl enable --now docker
+ sudo usermod -aG docker $USER

En este caso ya se tenia instalado Docker, como podemos observar a continuación:
<img width="1066" height="823" alt="imagen" src="https://github.com/user-attachments/assets/8aac2713-fa9a-451d-a5fd-4ff90bb57748" />

2. Como segundo paso iniciamos con la creacion del archivo, con los comando que ya habiamos visto en clase:

+ mkdir miapp
+ cd miapp

A continuación observamos que ya se creo el archivo y con "cd" podemos estar dentro de este mismo:
<img width="1055" height="81" alt="imagen" src="https://github.com/user-attachments/assets/9e162779-5f54-42c4-bdf5-2e25128029bb" />

3. Creamos el Dockerfile dentro del archivo con el comando:

+ nano Dockefile

Al ejecutar lo anterios, se abre una terminal para editar el dockerfile y escribimos lo que queremos que se ejecute, como se ve a continuación:
<img width="1864" height="903" alt="imagen" src="https://github.com/user-attachments/assets/01d8a970-2d04-46e3-a042-b69f763c3ecc" />

Se guarda  el archivo con cntrl + o, enter, y luego cntrl + x
<img width="1317" height="60" alt="imagen" src="https://github.com/user-attachments/assets/dca041b7-da28-43a9-8dd7-48fd4a687b29" />

4. Luego, de haber creado el dockerfile, procedemos a cronstruir la imagen:

+ docker build -t miapp:v1 .

La construcción de la imagen siempre tarda un poco mas en cargar, si al final te sale "Successfully built ..." es porque se construyo correctamente, como se ve a continuación:
<img width="1194" height="384" alt="imagen" src="https://github.com/user-attachments/assets/7224565f-5e6a-47aa-b717-c2304af5dd02" />
<img width="1198" height="333" alt="imagen" src="https://github.com/user-attachments/assets/ab32d438-a3ca-4d7d-99e6-0b86a6147cf7" />

4. Ahora iniciamos con la ejecucion:

+ docker run miapp:v1

Al ejecutar este comando ya nos deberia aparecer el comentario que se puso dentro del archivo del Dockerfile, como se ve aqui:
<img width="1219" height="82" alt="imagen" src="https://github.com/user-attachments/assets/dcbc1ea8-fc35-4819-899d-6de83dc413a8" />

### Referencias:

Kubernete:

+ Cloud Native Computing Foundation. (2024). Kubernetes Documentation. Recuperado de https://kubernetes.io/docs
+ Burns, B., Grant, B., Oppenheimer, D., Brewer, E., & Wilkes, J. (2016). Borg, Omega, and Kubernetes. Communications of the ACM.

Docke:

+ Docker Inc. (2024). Docker Documentation. Recuperado de https://docs.docker.com
+ Merkel, D. (2014). Docker: lightweight Linux containers for consistent development and deployment. Linux Journal.

### ITEM 3: Juego 

1. Inicamos creando el directorio del juego:
<img width="1342" height="77" alt="imagen" src="https://github.com/user-attachments/assets/f18ead61-9dfe-4ca2-9d45-98bb3f251ea6" />

2. Ahora creamos el archivo server.js:
<img width="1461" height="811" alt="imagen" src="https://github.com/user-attachments/assets/41b8d5f3-ea14-4929-a270-5e4a52a7326e" />

3. 
