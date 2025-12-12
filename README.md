
express.Router() --> used to create and maintain modular code while creating route handlers.

![image](https://github.com/user-attachments/assets/d96b5b79-da94-481c-8c5d-0f9ad186aef7)

![image](https://github.com/user-attachments/assets/5083b10b-e5d5-40b8-b6a4-7c2d9b22a751)





Packages we should be familiar when create express js app  - https://expressjs.com/en/resources/middleware.html

1) cookie-parser - This package makes the cookies sent in the header of any request to be available in the req object.

// Needed only for reading cookies
const cookieParser = require('cookie-parser');
app.use(cookieParser('secret')); // Optional secret enables signed cookies

// Setting cookies – doesn't need cookie-parser
app.get('/set', (req, res) => {
  res.cookie('lang', 'en', { maxAge: 900000 });
  res.send('Cookie set!');
});

// Reading cookies – needs cookie-parser
app.get('/get', (req, res) => {
  console.log(req.cookies); // { lang: 'en' }
  res.send(`Cookie value: ${req.cookies.lang}`);
});



--------------------------------------------------------------------------------------
1) NodeJs Streams -> Request , file read/write
2) NodeJs Buffers -> Array of Bytes
3) http -> http.createServer
4) path -> path__dirname
5) fs -> fs.createWriteStream, fs.createReadStream, fs.write, fs.writeSync, fs.read, fs.readSync
6) pipe -> pipe events
7) express js
8) app.use -> can attach a middleware which will be executed for all the request.
9) app.get -> will be executed only for get method and for that req url
10) req -> req.body (app.use(bodyParser.json()), req.method, req.url
11) res -> res.status(), res.send()
12) 
