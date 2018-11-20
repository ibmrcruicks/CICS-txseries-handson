# CICS-txseries-handson


## TXSeries for Multiplatforms

[TXSeries for Multiplatforms](https://www.ibm.com/uk-en/marketplace/txseries-for-multiplatforms)

![overview](/imgs/cicstx-overview.png)

Click on the [Try the CICS TXeries Beta (Windows, Linux, AIX)](https://hub.docker.com/r/ibmcom/txseries/) link - this will take you to instructions for creating a docker image running a local TXSeries server.

## Up and Running

You will need the current version of [Docker](https://www.docker.com/get-started) installed and running on your laptop/workstation, and an active internet connection.

Open a terminal window (shell, cmd, etc)

The following terminal command will 
+ create a docker container from ubuntu
+ install the TXSeries current beta 
+ configure the TXSeries default instance and activate the server
+ expose the web-admin port and the terminal server port (3270 emulator required for access)

```
docker run -it -p 3270:3270 -p 9443:9443 --name TXSERIES -e LICENSE=accept ibmcom/txseries
```

this will leave the docker session running in this command window, allowing you to see the runtime logs.

Open another terminal window and check on the docker process running TXSeries:
```
docker ps
```
You should see something similar to:
![cicstx-docker-ps](/imgs/cicstx-docker-ps.png)


### Installation Verification Program (IVP)
Connect to a terminal seession with x3270, [IBM Personal Communications](https://www.ibm.com/uk-en/marketplace/personal-communications), [tn3270 X for mac](https://www.brown.edu/cis/tn3270/index.html#latest),or similar host terminal emulator

Configure a terminal session with your emulator to connect to your localhost/loopback address on port 3270
```
tn3270 localhost:3270
```
This will bring up an empty 3270 terminal sesssion; to validate that the system is alive and well, enter `MENU` as the first transaction name

![Initial screen](/imgs/cicstx-initial-screen.png)

and press `ENTER` key.

![Installation verification - MENU](/imgs/cicstx-ivp-menu.png)
<br>
should be displayed.

### Web administration

Use the web admin tool to review and configure the server - the default admin username/password is *_txadmin/txadmin_*
<br>
![tx admin](/imgs/cicstx-web-admin.png)

Note that this is an *https* link which uses self-issued SSL certificates - you will likely need to add an exception to your browser to accept this.


