# CICS-txseries-handson


[TXSeries for Multiplatforms home page](https://www.ibm.com/uk-en/marketplace/txseries-for-multiplatforms)

[try the CICS TXeries Beta (Windows, Linux, AIX)](https://hub.docker.com/r/ibmcom/txseries/)


[Docker resource](https://hub.docker.com/r/ibmcom/txseries/)

[TxSeries admin](https://localhost:9443/txseries/admin)

```
docker run -it -p 3270:3270 -p 9443:9443 -e LICENSE=accept ibmcom/txseries
```

x3270, or similar host terminal emulator
( [tn3270 X for mac](https://www.brown.edu/cis/tn3270/index.html#latest) )

```
x3270 localhost:3270
```
will bring up an empty 3270 terminal sesssion; enter `MENU` as the first transaction name

![Initial screen](/imgs/cicstx-initial.png)

and press `ENTER` key.

![Installation verification - MENU](/imgs/cicstx-ivp-menu.png)
