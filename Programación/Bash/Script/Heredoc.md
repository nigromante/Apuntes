[[Bash]]

``` Syntax
[COMMAND] <<[-] 'DELIMITER'
  Line 1
  Line 2
  ...
DELIMITER
```

``` Ejemplo
cat << EOF
Hello
World
EOF
```
``` Variable-expansion
cat << END
$var1
$var2
$PWD
END
```
``` Command-expansion
cat << EOF
$(echo Hello)
$(whoami)
EOF
```
``` Ignore-Variable-and-Command-Expansion
cat << "EOF"
$(echo Hello)
$(whoami)
$PWD
EOF
```
``` Piping
cat << EOF | base64 -d
SGVsbG8KV29ybGQK
EOF
```
``` Piping-Alternate
(base64 -d) < cat << EOF
SGVsbG8KV29ybGQK
EOF
```
``` Write-to-file
cat << EOF > hello_world.txt
Hello
World
EOF
```
``` SFTP
sftp username@host << EOF
put test.sh
EOF
```