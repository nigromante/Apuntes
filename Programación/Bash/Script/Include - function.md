[[Bash]]

``` functions.sh
#!bin/bash

function dd() {
	echo "function dd"
}
```


``` main.sh
#!bin/bash
source "functions.sh"

dd 

```


