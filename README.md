[![Dependency Status](https://www.versioneye.com/user/projects/54f1ca554f3108d1fa00065a/badge.svg?style=flat)](https://www.versioneye.com/user/projects/54f1ca554f3108d1fa00065a)

##Lucee Application Template for Heroku
Blank application template to deploy Lucee 4.5.x (CFML/Java) apps on Heroku. 

**NOTE:** Lucee 5 version of this project available at [https://github.com/mikesprague/lucee5-heroku](https://github.com/mikesprague/lucee5-heroku)

[![Deploy](https://www.herokucdn.com/deploy/button.png)](https://heroku.com/deploy)

Demo: [https://lucee.herokuapp.com/](https://lucee.herokuapp.com/)

####Credits/Notes:
This began as a fork of Chris Blackwell's [railo-heroku-template](https://github.com/d1rtym0nk3y/railo-heroku-template) project. Recently, after [converting my fork of that project to Lucee](https://github.com/mikesprague/lucee-heroku-template/tree/905e19a9d863c504a86cd6a764a7a33805649546), I decided it had diverged enough to become it's own project and moved it to this repo. Many thanks to Chris for all of his original work and for inspiring this updated project for Lucee applications.

This project uses the [cfmlprojects.org](http://cfmlprojects.org/artifacts/org/lucee/) Maven repo maintained by [Denny Valliant](https://github.com/denuno). Many thanks to Denny for his work maintaining cfmlprojects.org.

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

To deploy your site to Heroku you need to setup a free Heroku account, install the Heroku toolbelt (Suggested reading: [Getting Started with Java on Heroku](https://devcenter.heroku.com/articles/getting-started-with-java)). Then..

```bash
$ heroku apps:create [NAME]
$ git push heroku master
$ heroku open
```

You should now be looking at your app running on Heroku.

Enjoy!
