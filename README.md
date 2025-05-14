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
