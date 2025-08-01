# Entorno de trabajo de Ansible con AWS

## Clonar el repositorio.
```
git clone https://github.com/ivolato/Desafio-6-Ansible.git
```

## Instalamos pipx en la maquina que usaremos para gestionar con Ansible.
```
sudo apt install pipx -y
pipx ensurepath
```

## Instalamos Ansible.
```
pipx install --include-deps ansible
```

## Verificamos que se instalo correctamente Ansible.
```
ansible --version
```

## Asignarle permisos correspondientes a la key para acceder por ssh.
```
cd Desafio-6-Ansible/.ssh
chmod 600 aws.pem
```

## Testeamos la coneccion con el nodo.
```
ssh -i ".ssh/aws.pem" ubuntu@[DIRECCION DEL EQUIPO]
```

## Ejecutamos el Playbook.
```
ansible-playbook -i inventory.ini site.yaml -v
```


