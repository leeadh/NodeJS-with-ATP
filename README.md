![capture](https://user-images.githubusercontent.com/15122358/44667149-93e07f80-aa4c-11e8-885e-4560f7edcbee.PNG)


This is a demo to showcase how to use Autonomous Transaction Processing (ATP) and connect with Node JS. This is using Node JS to render a simple HTML table and a simple post function which will write and commit to ATP database. The technology stack mainly used is Node JS which serves as our server and EJS as our templating engine. 

# Pre-requisites #
1) Log into your assigned ATP VM in the console using putty/ssh

2) There would be a folder called nodeJS_ATP. The folder structure is as shown below. 

![capture](https://github.com/leeadh/NodeJS-with-ATP/blob/master/overview.png)

There are a few folders we need to take note here

* wallet_ADRDEMO: This is our wallet which contains our unzipped ATP credentials. We will be changing this later to connect to your own ATP demo
* dbconfig: This is our ATP connection admin/password. We will be changing this later to connect to your own ATP demo
* dbconfig: OradbInstaClient: This is our instaclient needed to connect to ATP
* retrieveresultsJS/addresultsHS: This is our nodeJS file which will do a retrieval/add RESTFUL service from/to ATP
* OradbInstaClient: This is our instaclient needed to connect to ATP

 




