# cbt-tunnel-java
Java JAR for creating Local Connections to CrossBrowserTesting.com on the command line

#####Creates a local connection to CrossBrowserTesting.com via a Java Applet which allows you to test sites behind your firewall or to access web pages that are saved locally on your machine. 

In just a few seconds, you can establish a connection which allows you to do live testing, screenshots, or run Selenium scripts against any of the internal sites you have access to.

#####Instructions:

1. Ensure you have the latest Java JRE installed: http://java.com/en/download/
2. Download the cbttunnel.jar to your local machine.
3. Open a console to the directory of the downloaded jar in the previous step.
4. Run the appropriate command below.

There are three options for creating a Local Connection:

#####Internal websites:

	This directs requests from CBT browsers to your computer to test sites behind your firewall that would otherwise be inaccessible.

	java -jar cbttunnel.jar --authkey AUTHKEY

#####Local HTML Files:<br>

	This allows you to host static files on your computer that are not currently hosted on a server, as well as routing through your computer to access local or privileged sites.
	
	java -jar cbttunnel.jar --authkey AUTHKEY --dir "path/to/html"

#####Proxy Server:<br>
	The tunnel still routes through your computer to download site data, but it further directs that connection through a proxy of your choosing (always be wary in choosing a proxy--free and unsecure proxies are known to steal personal data).

	java -jar cbttunnel.jar --authkey AUTHKEY  -proxyip 192.168.1.100 -proxyport 8888

