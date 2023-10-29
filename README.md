Here we will use NodeJs to Create a server. It is javascript only but can be used in servers. 

 

1. Install nodeJs and npm on your PC, you can check out their website https://nodejs.org/en/download/

You can check if node and npm in installed or not in the terminal or windows shell with

node -v    // for node
npm -v     // for npm

2. Create a folder (my-webapp) where you want to create your project. Go to the folder and run the following command in your windows shell or terminal to initiate the node project 

npm init

You will be asked few information about the project. You can leave it empty and press Enter. It will create two files named package.json and package.lock.json these files will contain information about our project.

3. Install expressJs, this is a framework for nodejs which will help in creating a server and managing it. You can use the following command 

npm install express
It will install expressJs in our project. There is now a new folder created with the name node_modules  where all our installed files will go, you don't need to touch it for anything it is self-manageable.

4. Now create a server.js file and put the following content in it

var express = require('express');
var app = express();

const port = 3000;

app.get('/', function (req, res) {
    res.sendFile(__dirname+'/index.html');
});

app.listen(port, function () {
    console.log('listening on *:' + port);
});
If you are using windows use res.sendFile(__dirname+'\index.html');  on 7th line instead of  res.sendFile(__dirname+'/index.html');  as windows use forward slash (/) and ubuntu uses backward slash (\) for location of files.  

5. Create an HTML file with the name index.html and put the following sample HTML code in it. 

<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Welcome</title>
</head>

<body>
    <div style="font-size:30px; text-align: center; margin-top: 50px;">
        Hello there, <br>
        Congratulations !! on Building your web app ! <br>
        Keep Learning ! and Best Wishes from DApp World :)  
    </div>
</body>
</html>
Your folder should look like this

my-webapp   <-- This is your main project folder
|
-->node_modules         
-->index.html
-->package.json
-->package.lock.json
-->server.js
6. Run your server with the following command

node server.js
7. Now you can go to http://localhost:3000 to access the web app you created 

Congratulations on creating your server and web app


![image](https://github.com/thulasigithub123/Node_Express_Server/assets/87015668/386a9fd9-4d14-467d-a4df-48a444ff2ff6)
