# Ansible-Thinktic
Ejercicio02: Instalación de firewalld, openssh, nginx y mysql sobre una máquina Rocky a través de un único documento .yaml

Ejercicio03: Instalación de los servicios del ejercicio anterior, pero esta vez con separacion de tareas en diferentes documentos y llamada general en main.yaml. Además de la utilización de group_vars y diferenciación segun SO (debian y Rocky).

Ejercicio04: Instalación de docker completa, y tras esto la dockerización de los servicios de nginx, mysql y wordpress.

Ejercicio05: Pruebas con Ansible Vault, tags y lookups.

   En secret.yaml, el cual está codificado, encontraremos una función que ejecuta el comando date y
   nos imprime por pantalla su stdout.
    
   En task.yaml, encontraremos la llamada a una variable codificada y como según la llamemos su 
   aparición o no por pantalla. Además de diversas pruebas con los lookups:
   
   Tags:
   
        - Ports : with_items
        - lu : "{{lookup('file','variable.yaml')}}"
        - lu2 : "{{lookup('items','lista.yaml','lista2.yaml')}}"
        - lu3 : "{{lookup('nested','lista.yaml')}}"
