[[Bash]]
``` call.sh
#!/bin/bash

function call() {
	bash "$1.sh" "$2" "$3"
}
```

```called.sh
#!/bin/bash

	echo -e "Called script"

```

``` caller.sh
#!/bin/bash

	call "called"
	
```

	