# For the nodes stuck at block #3,699,041 

Open JS console with:
```
docker-compose exec testnet-validator-node geth attach /data/geth.ipc
```
Then set head to some blocks before:
``````
debug.setHead(web3.toHex(3690000))
``````
Close the console (ctrl+d) and restart the node:
````
docker-compose restart
`````
You may have proper peers connected to your node (check the note below).

If you still face wrong block issue, try again one more time.
If still no success, try to resync from 0 block and check the note below how to get the correct peers:
`````
docker-compose down -v --remove-orphans && docker-compose up -d
`````
