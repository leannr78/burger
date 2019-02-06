# burger
A restaurant app that lets users input the names of burgers they'd like to eat.  This uses MySQL to store the burger information and javascript.


https://frozen-escarpment-16189.herokuapp.com/burgers

Currently getting an error in heroku:  
2019-02-06T05:19:07.965206+00:00 app[api]: Enable Logplex by user leann.roberts@gmail.com2019-02-06T05:19:07.965206+00:00 app[api]: Release v2 created by user leann.roberts@gmail.com 2019-02-06T05:21:14.000000+00:00 app[api]: Build started by user leann.roberts@gmail.com
2019-02-06T05:21:31.555969+00:00 heroku[web.1]: Starting process with command `npm start`2019-02-06T05:21:36.674276+00:00 heroku[web.1]: State changed from starting to up
2019-02-06T05:22:52.998164+00:00 app[web.1]: /app/config/orm.js:33
2019-02-06T05:22:52.998174+00:00 app[web.1]: throw err;
2019-02-06T05:22:52.998176+00:00 app[web.1]: ^
2019-02-06T05:22:52.998178+00:00 app[web.1]:
2019-02-06T05:22:52.998180+00:00 app[web.1]: Error: Cannot enqueue Query after fatal error.
2019-02-06T05:22:52.998182+00:00 app[web.1]: at Protocol._validateEnqueue (/app/node_modules/mysql/lib/protocol/Protocol.js:200:16)
2019-02-06T05:22:52.998183+00:00 app[web.1]: at Protocol._enqueue (/app/node_modules/mysql/lib/protocol/Protocol.js:138:13)
2019-02-06T05:22:52.998185+00:00 app[web.1]: at Connection.query (/app/node_modules/mysql/lib/Connection.js:200:25)
2019-02-06T05:22:52.998187+00:00 app[web.1]: at Object.all (/app/config/orm.js:31:16)
2019-02-06T05:22:52.998188+00:00 app[web.1]: at Object.all (/app/models/burger.js:5:9)
2019-02-06T05:22:52.998190+00:00 app[web.1]: at /app/controllers/burgersController.js:13:10
2019-02-06T05:22:52.998192+00:00 app[web.1]: at Layer.handle [as handle_request] (/app/node_modules/express/lib/router/layer.js:95:5)
2019-02-06T05:22:52.998194+00:00 app[web.1]: at next (/app/node_modules/express/lib/router/route.js:137:13)
2019-02-06T05:22:52.998195+00:00 app[web.1]: at Route.dispatch (/app/node_modules/express/lib/router/route.js:112:3)
2019-02-06T05:22:52.998197+00:00 app[web.1]: at Layer.handle [as handle_request] (/app/node_modules/express/lib/router/layer.js:95:5)
2019-02-06T05:22:53.026972+00:00 app[web.1]: npm ERR! code ELIFECYCLE
2019-02-06T05:22:53.034207+00:00 app[web.1]: npm ERR! errno 1
2019-02-06T05:22:53.036009+00:00 app[web.1]: npm ERR! burger@1.0.0 start: `node server.js`
2019-02-06T05:22:53.036232+00:00 app[web.1]: npm ERR! Exit status 1
2019-02-06T05:22:53.036568+00:00 app[web.1]: npm ERR!
2019-02-06T05:22:53.036769+00:00 app[web.1]: npm ERR! Failed at the burger@1.0.0 start script.
2019-02-06T05:22:53.037030+00:00 app[web.1]: npm ERR! This is probably not a problem with npm. There is likely additional logging output above.
2019-02-06T05:22:53.060094+00:00 app[web.1]:
2019-02-06T05:22:53.060425+00:00 app[web.1]: npm ERR! A complete log of this run can be found in:
2019-02-06T05:22:53.060730+00:00 app[web.1]: npm ERR!     /app/.npm/_logs/2019-02-06T05_22_53_050Z-debug.log
2019-02-06T05:22:52.875773+00:00 heroku[router]: at=info method=GET path="/" host=frozen-escarpment-16189.herokuapp.com request_id=a2e2ec72-88bb-4ec8-b972-9bc6613e98ef fwd="24.18.194.216" dyno=web.1 connect=1ms service=45ms status=302 bytes=255 protocol=https
2019-02-06T05:22:53.018116+00:00 heroku[router]: at=error code=H13 desc="Connection closed without response" method=GET path="/burgers" host=frozen-escarpment-16189.herokuapp.com request_id=b53e2726-3494-4115-b18a-0761c2e06eaf fwd="24.18.194.216" dyno=web.1 connect=1ms service=30ms status=503 bytes=0 protocol=https
2019-02-06T05:22:53.146914+00:00 heroku[web.1]: Process exited with status 1
2019-02-06T05:22:55.042574+00:00 heroku[web.1]: Starting process with command `npm start`2019-02-06T05:22:57.631052+00:00 heroku[web.1]: State changed from starting to up
2019-02-06T05:23:03.729979+00:00 heroku[router]: at=info method=GET path="/favicon.ico" host=frozen-escarpment-16189.herokuapp.com request_id=4cf9e6a5-2994-47c2-b5e4-79651bfa11dc fwd="24.18.194.216" dyno=web.1 connect=5001ms service=14ms status=404 bytes=394 protocol=https
