# Ansible-LEMP

Es un pequeño ejemplo de cómo ejecutar un playbook de Ansible e instalar LEMP en un sistema operativo con Centos 7.

# 
# Como usarlo
Para poder ejecutar el pipeline de forma local teniendo Ansible instalado y en el directorio principal del playbook:

    ansible-playbook -i "localhost," -c local main.yml –k

Para ejecutar el mismo pipeline en otro host:

    ansible-playbook -i "<ip_addr>," main.yml –k

#
# NOTA

Con el flag `–k` solicitamos a ansible que nos pida contraseña para conectarnos con el host utilizando el usuario root.

Este playbook cuenta con testeo de Travis-CI el cual ejecuta todos los roles sobre un contenedor docker  que parte de una imagen de Centos-7, para poder ejecutarlo realizar un Pull Request al repositorio en github y acceder a Travis [https://travis-ci.org/nicocartalla/ansible-LEMP](https://travis-ci.org/nicocartalla/ansible)
