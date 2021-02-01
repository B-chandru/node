# node
## how to create a web server using node.js

* first install node.js.
* after installing node create a file with .js extension.
* now using the http package in node create a web server.
* the example is given below

### code

var http=require("http");  <br>

http.createServer((req,res)=>{ // to create a server<br>
    if(req.url==="/"){<br>
        res.end("Now you build a web server using node.js:)")
    }
    if(req.url==="/name"){
        res.end("hello everyone")
    }
    if(req.url==="/node"){
        res.end("it is a backend language");
    }
    if(req.url==="/time"){
        res.end(`<H1> ${new Date().toLocaleTimeString()}</H1>`); // u can use the browser api to display time,date,etc...
    }
    
}).listen(3000) // YOUR SERVER WILL LISTEN ON 3000
