# Supported tags and respective `Dockerfile` links

-	[`8`, `latest`] (*8/Dockerfile*)(https://github.com/kratochj/docker-tomcat/releases/tag/8)

# What is Tomcat?

Apache Tomcat (or simply Tomcat) is an open source web server and servlet container developed by the Apache Software Foundation (ASF). Tomcat implements the Java Servlet and the JavaServer Pages (JSP) specifications from Oracle, and provides a "pure Java" HTTP web server environment for Java code to run in. In the simplest config Tomcat runs in a single operating system process. The process runs a Java virtual machine (JVM). Every single HTTP request from a browser to Tomcat is processed in the Tomcat process in a separate thread.

[wikipedia.org/wiki/Apache_Tomcat)](wikipedia.org/wiki/Apache_Tomcat)


![logo](https://raw.githubusercontent.com/docker-library/docs/8e31eb93a02d504d0cfe1da435aa31b377fc627d/tomcat/logo.png)

# How to use this image.

Run the default Tomcat server (`CMD ["catalina.sh", "run"]`):

	$ docker run -it --rm tomcat:8.0

You can test it by visiting http://container-ip:8080 in a browser or, if you need access outside the host, on port 8888:

	$ docker run -it --rm -p 8888:8080 tomcat:8.0

You can then go to http://localhost:8888 or http://host-ip:8888 in a browser.

The default Tomcat environment in the image is:

	CATALINA_BASE:   /usr/local/tomcat
	CATALINA_HOME:   /usr/local/tomcat
	CATALINA_TMPDIR: /usr/local/tomcat/temp
	JRE_HOME:        /usr
	CLASSPATH:       /usr/local/tomcat/bin/bootstrap.jar:/usr/local/tomcat/bin/tomcat-juli.jar

The configuration files are available in `/usr/local/tomcat/conf/`. By default, no user is included in the "manager-gui" role required to operate the "/manager/html" web application. If you wish to use this app, you must define such a user in `tomcat-users.xml`.


# License

View [license information](https://www.apache.org/licenses/LICENSE-2.0) for the software contained in this image.

# Contributing

You are invited to contribute new features, fixes, or updates, large or small; we are always thrilled to receive pull requests, and do our best to process them as fast as we can.