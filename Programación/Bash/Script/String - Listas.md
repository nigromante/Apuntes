[[Bash]]

Convertir  un string a Lista

``` Space separator

read -a opciones <<< "uno dos tres"

```

``` Custom Separador 

IFS='|'

read -a opciones <<< "uno|dos|tres"

```
