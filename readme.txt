1) instalamos pipx en la maquina donde instalaremos ansible 
	En ubuntu:

- sudo apt install pipx -y
- pipx ensurepath

2) Instalamos Ansible

- pipx install --include-deps ansible

3) Verificamos la version

- ansible --version

4)creamos el archivo inventory.ini 

5)cambiar permisos de aws.pem

- chmod 600 aws.pem

6) Probamos acceder a nodo1 con la pem

- ssh -i "files/.ssh/aws.pem" ubuntu@[DIRECCION DEL EQUIPO]

7) ejecutamos el playbook

- ansible-playbook -i inventory.ini sete.yaml -v