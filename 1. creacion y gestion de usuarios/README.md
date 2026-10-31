
# Gestion y creacion de Usuario

Para ver que usuarios tienen asigando una bash


```
cat /etc/passwd | grep "sh$" | awk '{print $1}' FS=':'
```
o
```
cat /etc/passwd | grep "sh$" | cut -d ':' -f 1
```

para ver que usuario estoy actualmente 
```
whoami
```
para ver que grupos tenemos
```
id
```
si tenemos el sudo asignado podemos ser root con
```
sudo su
```
para crear un usuario le creamos su directorio home con
```
mkdir /home/pepito
```
```
useradd -d /home/pepito -s /bin/bash  pepito
```
para cambiarle la bash a un usuario listamos las que tenemos disponibles con 
```
cat /etc/shells
```
Para cambiarlo a Bash
```
sudo chsh -s /bin/bash pepito
```

para aignarle una contraseña
```
passwd pepito
```
dentro del /home cambiamos de grupo al directorio con
```
chown pepito:pepito pepito
```

