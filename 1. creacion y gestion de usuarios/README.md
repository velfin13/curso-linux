
# Gestion y creacion de Usuario

Para ver que usuarios tienen asigando una bash


```
cat /etc/passwd | grep "sh$" | awk '{print $1}' FS=':'
```
o
```
cat /etc/passwd | grep "sh$" | cut -d ':' -f 1
```
