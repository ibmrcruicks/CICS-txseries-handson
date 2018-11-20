# CICS-txseries-handson


[TXSeries for Multiplatforms home page](https://www.ibm.com/uk-en/marketplace/txseries-for-multiplatforms)

Click on the [Try the CICS TXeries Beta (Windows, Linux, AIX)](https://hub.docker.com/r/ibmcom/txseries/) link - this will take you to instructions for creating a docker image running a local TXSeries server.

```
docker run -it -p 3270:3270 -p 9443:9443 -e LICENSE=accept ibmcom/txseries
```

x3270, or similar host terminal emulator
( [tn3270 X for mac](https://www.brown.edu/cis/tn3270/index.html#latest) )

```
x3270 localhost:3270
```
will bring up an empty 3270 terminal sesssion; enter `MENU` as the first transaction name

![Initial screen](/imgs/cicstx-initial-screen.png)

and press `ENTER` key.

![Installation verification - MENU](/imgs/cicstx-ivp-menu.png)

Use the web admin tool to review and configure the server - the default admin username/password is *_txadmin/txadmin_*
<br>
![tx admin](/imgs/cicstx-web-admin.png)

Note that this is an *https* link which uses self-issued SSL certificates - you will likely need to add an exception to your browser to accept this.


