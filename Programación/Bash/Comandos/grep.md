[[Linux]]

``` archivo
hola mundo
hola loco
como estas
el mundo de la
programación funcionan
bien MUNDO 
```

``` normal
cat archivo | grep mundo 

hola mundo
el mundo de la

```
``` Ignore-case
cat archivo | grep -i mundo 

hola mundo
el mundo de la
bien MUNDO
```

``` Exclude
cat archivo | grep -v mundo 

hola loco
como estas
programación funcionan
bien MUNDO 
```

