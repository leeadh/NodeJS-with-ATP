![capture](https://user-images.githubusercontent.com/15122358/44667149-93e07f80-aa4c-11e8-885e-4560f7edcbee.PNG)


This is a demo to showcase how to use Autonomous Transaction Processing (ATP) and connect with Node JS. This is using Node JS to render a simple HTML table and a simple post function which will write and commit to ATP database. The technology stack mainly used is Node JS which serves as our server and EJS as our templating engine. 

# Pre-requisites #
1) Go to sql developer, connect to your ATP instance and execute the below script

https://github.com/leeadh/NodeJS-with-ATP/blob/master/sqlscript.sql

# Steps to connect to your ATP demo #
1) Log into your assigned ATP VM in the console using putty/ssh

2) There would be a folder called nodeJS_ATP. The folder structure is as shown below. 

![capture](https://user-images.githubusercontent.com/15122358/47579014-76ad2c00-d97d-11e8-838a-e40357259b4a.png)

There are a few folders we need to take note here

* wallet_ADRDEMO: This is our wallet which contains our unzipped ATP credentials. We will be changing this later to connect to your own ATP demo
* dbconfig: This is our ATP connection admin/password. We will be changing this later to connect to your own ATP demo
* dbconfig: OradbInstaClient: This is our instaclient needed to connect to ATP
* retrieveresultsJS/addresultsHS: This is our nodeJS file which will do a retrieval/add RESTFUL service from/to ATP
* OradbInstaClient: This is our instaclient needed to connect to ATP

 
 3) Unzip your wallet under the nodeJS_ATP folder. Now cd to your wallet location. i.e in this example ```cd wallet_ADRDEMO```. 
 
 Now do vi sqlnet.ora and change the Directory to be your wallet location. 
 
 ```
 i.e DIRECTORY="/nodeJS_ATP/oradbInstantClient/network/admin/<YOUR WALLET NAME>"
```

![capture](https://user-images.githubusercontent.com/15122358/47579070-980e1800-d97d-11e8-9079-a57774d793ab.PNG)

4) Now do ```export LD_LIBRARY_PATH=/home/opc/nodeJS_ATP/oradbInstantClient/instantclient_12_2```

5) Let us change our DB config file and make the necessary changes to your admin and password. ```vi dbconfig```. Change to your necessary connection details, password and admin details

![capture](https://user-images.githubusercontent.com/15122358/47579089-a6f4ca80-d97d-11e8-988a-9fc587cee605.PNG)

5) Go back to file directory ```cd ~/nodeJS_ATP```

6) Execute the following commands

```npm install```
```npm install oracledb --save```
```npm install express-flash-messages```

7) Finally lets run our node server. 

``` node server.js```

8) go to your ip address:5000

Your application should be serving as below

![capture](https://user-images.githubusercontent.com/15122358/47579104-af4d0580-d97d-11e8-97e8-9f3118a79294.PNG)

Now try doing insert into database and play with the application!
