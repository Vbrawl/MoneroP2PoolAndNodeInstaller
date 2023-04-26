# Description
This repository allows you to easily install monero to set up a node and p2pool.

They can be installed by running 2 simple commands.

They can also be uninstalled, again by running 2 simple commands.

# Install monero and setting up a node
```
./setup_node
```

After this completes, monero is installed.
The node now needs to synchronize.

Unfortunately, that has to be done manually.

```
./monero/monerod
```
If you'd like to run a prune blockchain, run:

```
./monero/monerod --prune-blockchain
```

Synchronization has started.
This process is going to take a lot of time (depending on your connection and hardware).

After synchronization is complete move on to installing p2pool.

# Install p2pool
```
./setup_p2pool
```

After this completes, p2pool is installed and you only need to start it.

to start p2pool you have to perform the following actions:

```
p2pool --host 127.0.0.1 --wallet <YOUR_WALLET_ADDRESS>
```


# Uninstall monero and the node
```
./purge_node
```

monero and the node are now removed from the system.


# Uninstall p2pool
```
./purge_p2pool
```

P2Pool is now removed!

Now you can choose wether you want to uninstall p2pool's dependencies

In order to remove all dependencies from your system you may run the following command:
```
sudo apt remove --purge git build-essential cmake libuv1-dev libzmq3-dev libsodium-dev libpgm-dev libnorm-dev libgss-dev libcurl4-openssl-dev libidn2-0-dev
```
