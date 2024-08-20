[[Linux]]

[crontab guru](https://crontab.guru/every-1-hour)



Manager
``` Manager 
crontab -e  #  Edit

crontab -l  #  List

crontab -r   # Reset
```


Estructura - Crontab
``` Estructura-Crontab
# .---------------- minuto (0 - 59) 
# | .------------- hora (0 - 23) 
# | | .---------- día del mes (1 - 31)
# | | | .------- mes (1 - 12) O ene, feb, mar, abr ... 
# | | | | .---- día de la semana (0 - 6) (domingo = 0 o 7) 
# | | | | | 
# * * * * * comando de nombre de usuario que se ejecutará 
```


Ejemplos
``` Ejemplos

0 0 * * * /usr/bin/jobs/midnight_tasks.sh  >/dev/null 2>&1 
0 * * * * /usr/bin/jobs/hourly_tasks.sh    >/dev/null 2>&1 

```
