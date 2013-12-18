JBoss BPM Suite Mortgage Demo 
=============================


![Install Console](https://github.com/eschabell/bpms-mortgage-demo/blob/master/docs/demo-images/install-console.png?raw=true)

![Mortgage Process](https://github.com/eschabell/bpms-mortgage-demo/blob/master/docs/demo-images/mortgage-process.png?raw=true)


Quickstart
----------

1. Clone project.

2. Add products to installs directory.

3. Run 'init.sh' or 'init.bat' file.

4. Login to http://localhost:8080/business-central  (u:erics / p:bpmsuite)

  - login for appraisor role (u:alan / p:bpmsuite)

  - login for broker role (u:bob / p:bpmsuite)

  - login for manager role (u:mary / p:bpmsuite)


Notes
-----
The following functionality is covered:

- One advanced process.

- Four Human Tasks assigned to 3 different roles

- Use of Swimlanes to assign a task to the user who previously took ownership

- Several guide business rules

- Several technical rules

- A guided web decision table

- Several Script Tasks for Java work

- One Web Service task using SOAP/HTTP

- Exclusive use of the BPMS Data Modeler for creating the Java fact model

- Use of graphic form designer to create 4 forms with an example of javascript validation

- Helper jar to pre-load with sixteen process instances in various states.

Note that the entire demo is running default in memory, restart server, lose your process instances, data, monitoring history.


Mortgage demo known issues 
--------------------------

Project is broken for Beta right now. Init.sh disabled to not install demo project nor demo project web service.

- client jar is currently defective, will not populate the instances.

- login gives errors but UI continues to work.

- web service call fails in process, workaround below is not working for me.

- issues with work items, here is a workaround:

    - go to target/jboss-eap-6.1/standalone/deployments/business-central.war/WEB-INF/classes/META-INF and move the
		  following two files to your home directory:

         - drools.session.conf
 
         - CustomWorkItemHandlers.conf



Supporting Articles
-------------------

[Red Hat JBoss BPM Suite - installing the Mortgage demo project (video)] (http://www.schabell.org/2013/10/jboss-bpm-suite-install-mortage-demo-video.html)

[Red Hat JBoss BPM Suite - get rocking with the all new Mortgage Demo] (http://www.schabell.org/2013/10/jboss-bpm-suite-rocking-the-mortgage-demo.html)


Released versions
-----------------

See the tagged releases for the following versions of the product:

- v0.4 - JBoss BPM Suite 6.0.0.Beta, JBoss EAP 6.1.1, and mortgage demo installed.

- v0.3 - JBoss BPM Suite 6.0.0.Beta1, JBoss EAP 6.0, and mortgage demo installed.

- v0.2 - JBoss BPM Suite ER4, JBoss EAP 6.0, new roles assignment, and mortgage demo installed.

- v0.1 - JBoss BPM Suite ER3, JBoss EAP 6.0, and mortgage demo installed.
