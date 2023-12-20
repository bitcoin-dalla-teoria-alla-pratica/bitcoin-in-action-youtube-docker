# Docker Bitcoin in Action Youtube (rete Regtest)

<img src="https://i.ibb.co/CsLN0J2/bitcoin-Docker.png">


Per utilizzare questo repository, per prima cosa è necessario clonarlo.
```bash
git clone https://github.com/bitcoin-dalla-teoria-alla-pratica/bitcoin-in-action-youtube-docker --depth 1
cd bitcoin-in-action-youtube-docker
```
Successivamente sarà necessario clonare il repository del canale youtube

```bash
git clone https://github.com/bitcoin-dalla-teoria-alla-pratica/Bitcoin-in-Action --depth 1
```

Infine dobbiamo lanciare il comando


```bash

docker-compose up

```

# Come utilizzare gli esempi del libro
Ipotizziamo di voler replicare l'esempio del video 1

Entriamo dentro il container.
Individuiamolo con il comando
```bash
docker ps
```
e utilizziamo il valore sotto la colonna NAMES, ad esempio
```bash

docker exec -it docker exec -it bitcoin-in-action-youtube zsh zsh

```
Successivamente ci muoviamo dentro la cartella dei video
```bash
cd Bitcoin-in-Action
```

Identifica il video che vuoi provare (disponibile dal video 12 in poi) e lancia

```bash
./main.sh
```

Se vogliamo attivare il debug della transazione sarà necessario utilizzare il parametro DEBUG=1
```bash
./main.sh DEBUG=1
```
Questo grazie al progetto [btcdeb](https://github.com/bitcoin-core/btcdeb)

# Utilizzo di btc-rpc-explorer su Regtest

Grazie al progetto [btc-rpc-explorer](https://github.com/janoside/btc-rpc-explorer), ora abbiamo a disposizione un explorer su regtest. Questo ci consente di visualizzare quanto sta accadendo nella rete regtest di Bitcoin attraverso un'interfaccia grafica.

Per accedere all'explorer, collegati a [http://localhost:3002/](http://localhost:3002/) e avrai a disposizione una GUI per esplorare la rete regtest.


## Per uscire dal container
Per uscire dal container
```bash
exit
```

successivamente per fermare e rimuovere il container utilizzare il comando

```bash
docker-compose down
```