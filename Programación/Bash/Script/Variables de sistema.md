[[Bash]]

| **Variable especial** | **Explicación**                                                         |
| --------------------- | ----------------------------------------------------------------------- |
| $@                    | Almacena argumentos como un array                                       |
| $$                    | Muestra el ID del proceso de la shell actual                            |
| $#                    | Muestra el número de argumentos proporcionados en un determinado script |
| $*                    | Agrupa todos los argumentos dados conectándolos                         |
| $!                    | Muestra el ID del último trabajo en segundo plano                       |
| $?                    | Muestra el código de estado de salida para el último comando ejecutado  |
| $0                    | Muestra el nombre del archivo del script actual                         |
| $_                    | Asigna la variable al último argumento del último comando               |
| $-                    | Muestra las banderas actualmente utilizadas en la shell de bash         |
| $1-${11}              | Almacena datos de los primeros 11 nombres de argumentos                 |
