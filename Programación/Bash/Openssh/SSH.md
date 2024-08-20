[[Linux]]
``` conexion-Normal
ssh -p 22 user@host
```


# PROXY

``` 
ssh -D <port> <user>@<hop_host>
```
# TUNEL

LOCAL

```
$ ssh -L <local_port>:<target_host>:<target_port> <user>@<hop_host>
```

``` Where

- `<local_port>` => Port that we want to open on the loopback interface (`lo`) of our computer as a result of the SSH tunnel. If port number to be opened is less than 1024 (privileged ports, such as 80 or 443), the ssh command must be run with root privileges.

- `<target_host>` => Hostname or IP address associated to the target service against which we wish to establish a connection.

- `<target_port>` => Port associated to the target service against which we wish to establish a connection.

- `<user>` => User through who we have SSH accessto the hop machine (intermediate server).

- `<hop_host>` => Hostname or IP address associated to the hop machine (intermediate server).
```

```  SCRIPT
#!/bin/bash

HOP_HOST="[-i <priv_key_file_path> ]<user>@<hop_host>"
TARGET_HOST=<target_host>
TARGET_PORT=<target_port>

PORT_FORWARDING="1$TARGET_PORT:$TARGET_HOST:$TARGET_PORT"
PID=$(/bin/ps -ef |grep "$PORT_FORWARDING" |grep -v grep |awk '{print $2}')
if [[ -z $PID ]]
then
    /usr/bin/ssh -fN -g -L $PORT_FORWARDING $HOP_HOST
else
    echo -e "\nThe SSH tunnel is already running with process ID => ${PID}\n"
    exit 1
fi

PID=$(/bin/ps -ef |grep "$PORT_FORWARDING" |grep -v grep |awk '{print $2}')
echo -e "\nFanfare! SSH tunnel up & running in the local port 1$TARGET_PORT!"
echo -e "\nProcess ID of SSH tunnel => ${PID}\n"
```





REMOTO

```  Syntax

ssh -R [remote_port]:[destination_address]:[local_port] [username]@[ssh_server]

```