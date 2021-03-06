Project:  Eclipse Paho MQTT Client View
Version:  1.0.0
Date:     06-06-2012
Author:   Eurotech Inc.


**************
** Overview **
**************

The Eclipse Paho MQTT Client View is an Eclipse plug-in that provides a 
user interface for managing an MQTT client within Eclipse.  


******************
** Installation **
******************

The plug-in can be installed using the included update site:

 update_site/update.site.zip
 
1) Unzip the file onto your local machine.  

2) In Eclipse, browse to Help -> Install New Software.

3) Add a new local repository by clicking on the "Add..." button and browsing to the directory
that you unzipped above (should contain a site.xml file).  Make sure to name the repository
and then click "Ok".  You should now be able to select the repository in the "Work with:" 
drop down menu and the plug-in should appear in the list.  

4) Select the plug-in:

 Paho Client Eclipse View Feature
	
5) Click "Next" and follow the remaining instructions for installing the plug-in.


***********
** Usage **
***********

The view can be accessed by navigating to Window -> Show View -> Other..., then expand the 
"Others" folder and select "Eclipse Paho Client View".  This will open the interface for the 
Paho MQTT client.  The interface consists of three tabs: Connection, Publish, and Subscribe.

-Connection Tab

This tab is used to connect the MQTT client to a broker.  A connection
must be established in order to publish and subscribe in the remaining
tabs.  Here is a brief description of the fields:

Broker Address: (Required) The IP address or URL of the broker
Broker Port:    (Required) The port number of the broker
Client ID:      (Required) A unique identifier to connect with.
Username:       A username, if required by the broker.
Password:       A password, if required by the broker.
Keep Alive:     (Required) The number of seconds between keep alive pings sent to the broker.
Clean Start:    Whether or not to maintain subscriptions across disconnects.
LWT Enable:     Whether to enable Last Will and Testament (LWT).
LWT Topic:      The topic that the broker will publish the LWT on.
LWT Message:    The message that the broker will publish for the LWT.
LWT QoS:	The quality of service that the LWT will be published on.
LWT Retain:	Whether to retain the LWT message.

-Publish Tab

Used to publish messages to the broker.  A message may be a string or a File.  Here is a 
brief description of the fields:

Topic:	 The topic to publish on.
QoS:     The quality of service to publish on.
Payload: The payload to publish (if publishing a string).
File:    The file to publish (if publishing a file).

-Subscribe Tab

Used to subscribe and unsubscribe on topics.  Once the client is subcribed to a topic, all 
messages recieved will be displayed to the log below.  Here is a brief description of the 
fields:

Topic: The topic to subscribe on.
QoS:   The quality of service to subscribe on.


**************
** Building **
**************

The project requires the Plug-in Development Environment (PDE) in order to build. 
Information about installing the PDE tools can be found at: 

 www.eclipse.org/pde
	
The source for the project itself can be found at:

 http://git.eclipse.org/c/paho/org.eclipse.paho.mqtt.java.git/
	
Once the project is imported into Eclipse, it can be build by rigt clicking on the project
and navigating to Export -> Plug-in Developement -> Deployable plug-ins and fragments.


***************
** Copyright **
***************

Copyright (c) 2012 Eurotech Inc. All rights reserved.


*************
** License **
*************

This project is released under the Eclipse Public License (EPL) version 1.0


******************************
** Additional Documentation **
******************************

Eclipse Paho:  http://www.eclipse.org/paho/
MQTT:          http://www.mqtt.org

