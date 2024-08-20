[[Bash]]

	No se pueden nombrar los parámetros
	
``` 
#!/bin/bash

function fn() {
	echo "function dd:: $1 ó ${1} "
	printf -v "result" "123"
}


fn "parametro"
echo $result


```

```return-ejemplo
#!/bin/bash

addition() {
	sum=$(($1+$2))
	return $sum
}

read -p "Ingresa un número: " int1
read -p "Ingresa un número: " int2

addition $int1 $int2

echo "El resultado es : " $?
```

