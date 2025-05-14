
express.Router() --> used to create and maintain modular code while creating route handlers.

![image](https://github.com/user-attachments/assets/d96b5b79-da94-481c-8c5d-0f9ad186aef7)

![image](https://github.com/user-attachments/assets/5083b10b-e5d5-40b8-b6a4-7c2d9b22a751)





Packages we should be familiar when create express js app

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
