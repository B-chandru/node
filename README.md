# node
## how to create a web server using node.js

* first install node.js.
* after installing node create a file with .js extension.
* now using the http package in node create a web server.
* the example is given below

### code

var http=require("http");  <br>

http.createServer((req,res)=>{ &nbsp;// to create a server<br>
    if(req.url==="/"){  <br>
        res.end("Now you build a web server using node.js:)")<br>
    } <br>
    if(req.url==="/name"){<br>
        res.end("hello everyone")<br>
    }<br>
    if(req.url==="/node"){<br>
        res.end("it is a backend language");<br>
    }<br>
    if(req.url==="/time"){<br> 
        res.end(`<H1> ${new Date().toLocaleTimeString()}</H1>`); &nbsp;// u can use the browser api to display time,date,etc...<br>
    }<br>
    
}).listen(3000)&nbsp; // YOUR SERVER WILL LISTEN ON 3000<br>
