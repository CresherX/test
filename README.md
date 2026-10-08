const os = require("os");
const http = require("http");
const userName = os.userInfo().username;

http.createServer(function(request,response){
    response.end('Hello,' + userName);
}).listen(3000, "127.0.0.1", function(){
    console.log("Прослушивание на порту 3000");
});
