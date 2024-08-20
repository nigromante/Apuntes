[[SSH]]
``` Syntax

scp [other options] [source username@IP]:/[directory and file name] [destination username@IP]:/[destination directory]

```
Options

```
- –P port permite especificar una entrada diferente al servidor (el puerto predeterminado para el puerto TCP para el comando es 22)

- –c cipher te da la posibilidad de especificar el algoritmo de cifrado que utilizará el cliente. Algunos de los valores que puedes usar son ‘aes256-ctr’, ‘aes256-cbc’, ‘blowfish-cbc’, ‘arcfour’, ‘arcfour128’, ‘arcfour256’, ‘cast128-cbc’, aes128-ctr’, ‘aes128-cbc’, ‘aes192-ctr’, ‘aes192-cbc’, y 3des-cbc’. La opción predeterminada en la configuración de shell es ‘AnyStdCipher’
 
- –q ejecutará la operación en modo silencioso (quiet), lo que significa que solo se mostrarán los errores críticos.
 
- –r es para copia recursiva, que incluirá todos los subdirectorios.
 
- –4 o -6 se pueden usar si quieres elegir la versión de protocolo empleada, ya sea IPv4 o IPv6. También puedes configurar los requisitos de dirección IP de manera más exhaustiva con la palabra clave de la familia de direcciones (address-family keyword).
 
- –p conservará los tiempos de modificación iniciales y los atributos del archivo.
 
- –u borrará el archivo fuente después de que se complete la transferencia.
 
- –c permitirá la compresión de los datos mientras se lleva a cabo la operación de transferencia.

```

Local - Remoto
``` Simple  
scp /users/Edward/desktop/scp.zip root@191.162.0.2:/writing/article
```
``` Port
scp -P 2322 /users/Edward/desktop/scp.zip root@191.162.0.2:/writing/article
```
``` Recursivo
scp -r /users/Edward/desktop root@191.162.0.2:/writing/article
```



Remoto - Local 
```
scp root@191.162.0.2:/writing/articles/SCP.zip Users/Edward/Desktop
```


Remoto - Remoto
```
scp root@191.162.0.2:/writing/article/scp.zip edward@11.10.0.1:/publishing
```
``` Pasa-por-el-equipo-local
scp -3 root@191.162.0.2:/writing/article/scp.zip edward@11.10.0.1:/publishing
```

