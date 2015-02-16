##Lucee Application Template for Heroku
Blank application template to deploy Lucee (CFML/Java) apps on Heroku

[![Deploy](https://www.herokucdn.com/deploy/button.png)](https://heroku.com/deploy)
Demo: [https://lucee.herokuapp.com/](https://lucee.herokuapp.com/)

####Credits/Notes:
This began as a fork of Chris Blackwell's [railo-heroku-template](https://github.com/d1rtym0nk3y/railo-heroku-template) project. Recently, after [converting my fork to Lucee](https://github.com/mikesprague/lucee-heroku-template), I decided it had diverged enough to become it's own project and moved it to this repo. 

###Requirements
* [Maven](http://maven.apache.org/) to build the project
* [Foreman](https://github.com/ddollar/foreman) to run locally

###Instructions
To get started, run the following commands in GitBash (or your terminal of preference):

```bash
$ git clone https://github.com/mikesprague/lucee-heroku.git
$ cd lucee-heroku
$ mvn package
$ foreman start
```
NOTE: On Windows, start foreman with the following command: 
```bash
$ foreman start -f Procfile.dev
```

You should now have Lucee up and running at [http://localhost:5000](http://localhost:5000).
Start adding your code to /webroot.

By default, access to the Lucee server/web admins has remote access blocked. This can be 
configured in /webroot/WEB-INF/urlrewrite.xml

To deploy your site to Heroku you need to setup a free Heroku account, install the Heroku toolbelt (you can find their getting started guide [here](https://devcenter.heroku.com/articles/quickstart)). Then..

```bash
$ heroku apps:create [NAME]
$ git push heroku master
$ heroku open
```

You should now be looking at your app running on Heroku.

Enjoy!
