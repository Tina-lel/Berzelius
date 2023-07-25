# Berzelius

An end to end encrypted chat room using GPG's AES256 cypher, supporting multiple users written entirely in bash with the help of socat.

Dependencies:
-
bash

socat

gpg

Ussage:
-

```
git clone https://github.com/Tina-lel/Berzelius
```
## server:

```
cd Berzelius/server
```

```
chmod +x server
```

open up "config" in a text editor and choose a port number to replace "1234", "1235" and "12346", and optionally forward these ports in your gateways configuration page, to communicate outside of your internal network.

```
./server
```

see "Commands" for a list of valid commands

#### entering a password and running the server:

```
pass
```

the password file was generated in (script location)/gpg you should be careful with it (ITS PLAIN TEXT)

```
start
```

if everything went fine, and the server didn't return any errors, you can test the connection with a client

## client:

```
cd Berzelius/client/
```
```
chmod +x client
```

open up "config" in a text editor and edit the "example" server function to point to a machine running the server script on the same ports. you can add as many server functions as you'd like.

```
./client
```

enter a server function name (a name before the "()" in the config)

enter the server's password

if the server was running, and everything went fine, you should now see a blank screen, with a little arrow.

in order to chat, type something and press enter. type "!q" to disconnect and exit (CTRL+C also works)

Commands:
-

### server:

help: this message

pass: set password

start: start the server

stop: kill the server

exit: exit the script

### client (in chat):

!help / !h (help message)

!scroll / !s (view chat history)

!back / !b (disconnect and return)

!quit / !q (disconnect and exit)
