# node
## how to create a web server using node.js

* first install node.js.
* after installing node create a file with .js extension.
* now using the http package in node create a web server.
* the example is given below

### code
<pre>
<code>
var http=require("http");  

http.createServer((req,res)=>{ &nbsp;// to create a server
    if(req.url==="/"){  <br>
        res.end("Now you build a web server using node.js:)")
    }
    if(req.url==="/name"){
        res.end("hello everyone")
    }
    if(req.url==="/node"){
        res.end("it is a backend language");
    }
    if(req.url==="/time")
        res.end(`<H1> ${new Date().toLocaleTimeString()}</H1>`); &nbsp;// u can use the browser api to display time,date,etc...
    }
    
}).listen(3000)&nbsp; // YOUR SERVER WILL LISTEN ON 3000
</code>
</pre>
