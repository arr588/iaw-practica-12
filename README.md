# Práctica 12

## Amazon Machine Image (AMI) de Bitnami para WordPress

- Instalamos la AMI de Bitnami desde [este enlace](https://bitnami.com/stack/wordpress/cloud/aws/amis):

![ami](https://raw.githubusercontent.com/arr588/iaw-practica-12/main/img/1.png?token=ALTEBMVUJYTJSODKADORYDLARJVN4)

![AWS](https://raw.githubusercontent.com/arr588/iaw-practica-12/main/img/2.png?token=ALTEBMSZWPS4AGN3LBLUYMDARJV5Y)

- Para buscar el usuario y la contraseña para Wordpress entramos en el registro de sistema desde AWS:

![registro-1](https://raw.githubusercontent.com/arr588/iaw-practica-12/main/img/3.png?token=ALTEBMQPX2AMGQ7FDSVGYE3ARJWQK)

![registro-2](https://raw.githubusercontent.com/arr588/iaw-practica-12/main/img/4.png?token=ALTEBMRJZXFBDD63LGV7RRLARJWRC)

- Cogemos la IP de la máquinad de Bitnami y accedemos al panel de administración de Wordpress con el usuario y la contraseña que hemos obtenido:

![wp-admin](https://raw.githubusercontent.com/arr588/iaw-practica-12/main/img/5.png?token=ALTEBMUXAFJNQ3WVHZSLNRLARJXCS)

- Para poder acceder a phpMyAdmin tendremos que hacer un tunel inverso desde nuetra máquina hasta el panel de php de la máquina de Bitnami. Para ello lo haremos desde Powershell usando el comando:

    `ssh -N -L 8888:127.0.0.1:80 -i C:\Users\djale\Desktop\Claves\clave_prac01.pem bitnami@54.89.9.147`

![phpmyadmin](https://raw.githubusercontent.com/arr588/iaw-practica-12/main/img/6.png?token=ALTEBMUO7YTU57L4PPSEBGLARJXVA)