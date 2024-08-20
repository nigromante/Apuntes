[[Bash]]
``` Prompt
read -p "Enter your username: " username
```
```  Hide
read -p "Enter your password: "$'\n' -s password
```
``` Limit
read -n 3
```
``` Timeout
read -t 5
```
``` Array
read -a array <<< "Hello world!"
```
``` Ignore-backslash-intrepretation
read -r <<< "Hello\world!"; echo $REPLY
```

``` Heredoc-Notation
read var1 var2 <<< "Hello world!"
echo $var1
echo $var2
```
