04/05/2017

What is ubertask optimization?
	* optimize the time for running the Uber jobs in MapReduce. It allows to run mapper and reducers in the same process as the ApplicationMaster (AM)

Where in CM is the Kerberos Security Realm value displayed?
	* HDFS - Configuration - Security - Trusted Kerberos Realms
	
Which CDH service(s) host a property for enabling Kerberos authentication?
	* Zookeeper, HDFS, YARN

How do you upgrade the CM agents?
	* upgrade the JDK on the agent, upgrade Cloudera Manager, then there is a wizard from the CM 

Give the tsquery statement used to chart Hue's CPU utilization?
	* click on Hue, the on the top right corner Open in Chart Builder
	
Name all the roles that make up the Hive service
	* click on the Hive service, then "Instances"

What steps must be completed before integrating Cloudera Manager with Kerberos?	
	* Get or Create a Kerberos Principal for the Cloudera Manager Server
	* Enabling Kerberos Using the Wizard
	* Create the HDFS Superuser
	* Get or Create a Kerberos Principal for Each User Account
	* Prepare the Cluster for Each User
	* Verify that Kerberos Security is Working
	* Enable Authentication for HTTP Web Consoles for Hadoop Roles