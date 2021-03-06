Spring Boot 1.5.x and Angular 4.x with HTML 5 router
====================================================

This project provides an example of an Angular single page application, served by ``Tomcat``,
configured with the ``html5 router``.

The [ForwarderController](src/main/java/com/mpalourdio/html5/mvc/ForwarderController.java) acts like a replacement for mod_rewrite : It forwards every single request that match ``context path`` to index.html.

It's useful if you want to serve an Angular application with the ``html5 router``, and avoid the dashed URL.

This ``html5 router`` mode makes pretty URL, but has a default : Refreshing pages (or accessing them directly) gives a 404
http error if no RewriteRule is provided by the http server that serve the application or by an .htaccess.

Static files in ``src/main/resources`` have been put in a [static](/src/main/resources/static/static) subfolder, just to show the possibility to
put them on a front-end reverse proxy that could serve the application assets.

To test the project, run [Application](src/main/java/com/mpalourdio/html5/Application.java), and point your browser to [http://localhost:10000/my-context](http://localhost:10000/my-context).

If you want to play with the front part, go to the [front folder](front). Once you have built the project, put the files in [src/main/resources/static](src/main/resources/static).

The front-end part has been scaffolded with [angular-cli](https://github.com/angular/angular-cli).

