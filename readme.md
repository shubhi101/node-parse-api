Node Parse API
==============

install
-------

    npm install parse-api

examples
--------

### setup

    var Parse = require('parse-api').Parse;
    
    var APP_ID = ...;
    var MASTER_KEY = ...;
    
    var app = new Parse(APP_ID, MASTER_KEY);

### insert

    // add a Foo object, { foo: 'bar' }
    app.insert('Foo', { foo: 'bar' }, function (err, response) {
      console.log(response);
    });

### find one

    // the Foo with id = 'someId'
    app.find('Foo', 'someId', function (err, response) {
      console.log(response);
    });

### find many

    // all Foo objects with foo = 'bar'
    app.findMany('Foo', { foo: 'bar' }, function (err, response) {
      console.log(response);
    });

### update

    app.update('Foo', 'someId', { foo: 'fubar' }, function (err, response) {
      console.log(response);
    });

### delete

    app.delete('Foo', 'someId', function (err) {
      // nothing to see here
    });
