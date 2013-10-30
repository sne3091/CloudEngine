CloudEngine
===========

Open source backend for mobile


Overview
=========

CloudEngine is an open source backend stack for building awesome mobile apps.
The aim of the project is to help mobile app developers get their apps off the ground
as quickly as possible. For this, CloudEngine needs to provide all the basic services
required for building rich mobile apps out-of-the-box. Currently there are bare minimum
services included. The aim is also to create fully customizable and extensible framework for
building backend mobile services. The core services could be tightly coupled.


Requirements
=============

* Python (2.7.5+)
* Django (1.5+)

Installation
===============

Clone the project. Configure database and other necessary 
settings in `cloudengine.settings.py`. Create database tables.

	manage.py syncdb
	
Run the server 

	manange.py runserver
	
	
Technical Overview
====================

CloudEngine is a pure Python django stack. Each backend service is plugged in as django
app. Each service should be independently pluggable and usable except the core services. 
Currently some of the services are tightly coupled. CloudEngine uses the excellent
[gevent-socketio][gevent-socketio] library for implementing real time communication
channels, which are the basis of current push notifications system. 
gevent-socketio is the python port of the popular [socket.io][socket.io] library. 


Client libraries
==================

The aim of the project is also to provide readily available client libraries for 
as many different platforms as possible to make it easier to consume CloudEngine
services on mobile devices.
Currently only Android SDK is available at -  [https://github.com/cloudengine/Android-SDK][android-sdk]
We plan to add SDKs for more platforms 


Documentation & Support
========================

Complete documentation is available at - ?

For discussions, questions and support use the [CloudEngine discussion group][group]

or [Github issue tracking][issue-tracker]

You may also want to [follow the authors on twitter] [twitter]. 



License
========
See the LICENSE file for more info.



[twitter]: https://twitter.com/thecloudengine
[group]: https://groups.google.com/forum/#!forum/cloudengine-dev
[gevent-socketio]: https://github.com/abourget/gevent-socketio
[socket.io]: http://socket.io
[issue-tracker]: https://github.com/cloudengine/CloudEngine/issues
[android-sdk]: https://github.com/cloudengine/Android-SDK
