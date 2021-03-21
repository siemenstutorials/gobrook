## Run brook wssserver

Make sure your domain name has been successfully resolved, brook will automatically issue certificate for you, assume your domain is `domain.com`. If there is a firewall, remember to allow TCP on this port 80 and 443.

```
$ brook wssserver --domain domain.com --password hello
```

> More parameters: $ brook wssserver -h

Then your brook wsserver is: `wss://domain.com:443`

---

## Run in background via `nohup`

> We recommend running the command directly to make sure there are no errors before running it via nohup

```
$ nohup brook wssserver --domain domain.com --password hello &
```

Stop background brook

```
$ killall brook
```

---

## Run as daemon via [`joker`](https://github.com/txthinking/joker) 🔥

> We recommend running the command directly to make sure there are no errors before running it with joker

```
$ joker brook wssserver --domain domain.com --password hello
```

View running commmands via joker

```
$ joker list
```

Stop a running command via joker

> Your can get ID from output by $ joker list

```
$ joker stop <ID>
```

View log of a command run via joker

> Your can get ID from output by $ joker list

```
$ joker log <ID>
```

---

## Auto start at boot via [`boa`](https://github.com/brook-community/boa)

> We recommend running the command directly to make sure there are no errors before running it via boa

```
$ boa brook wssserver --domain domain.com --password hello
```

Or with joker

```
$ boa joker brook wssserver --domain domain.com --password hello
```
