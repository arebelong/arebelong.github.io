---
layout: post
date:   2014-10-16 07:26:44
categories: blog
tags: ["nodejs","passport"]
---
sudo apt-get install lmms 
How to setup user authentification

[http://passportjs.org/guide/](http://passportjs.org/guide/)


	npm install passport --save-dev

	npm install passport-local --save-dev

	npm install express-session --save-dev

Documentation is lagging...

https://github.com/expressjs/session





var passport = require('passport')
  , LocalStrategy = require('passport-local').Strategy;

passport.use(new LocalStrategy(
  function(username, password, done) {
    User.findOne({ username: username }, function(err, user) {
      if (err) { return done(err); }
      if (!user) {
        return done(null, false, { message: 'Incorrect username.' });
      }
      if (!user.validPassword(password)) {
        return done(null, false, { message: 'Incorrect password.' });
      }
      return done(null, user);
    });
  }
));


app.post('/login', 
  passport.authenticate('local', { failureRedirect: '/login' }),
  function(req, res) {
    res.redirect('/');
  });
