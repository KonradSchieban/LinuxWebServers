# LinuxWebServers

<h2>General Information</h2>
<ul>
  <li>FQDN: ec2-52-41-123-95.us-west-2.compute.amazonaws.com
  <li>Public IP address: 52.41.123.95
  <li>SSH Port: 2200
  <li>URL to Catalog App: http://ec2-52-41-123-95.us-west-2.compute.amazonaws.com/
</ul>

<h2>Summary of Configuration Changes</h2>
<ol>
  <li>User <i>grader</i> added with sudo permissions
  <li>Timezone has been set to UTC using dpkg-reconfigure tzdata
  <li>SSH port has been set to 2200 by adjusting the sshd_config file
  <li>All ports have been closed by default except ports 2200 (SSH), 80 (HTTP), 123 (NTP) using UFW
  <li>A user </i>catalog</i> has been created who only has permissions to modify the database catalogapp
  <li>All packages have been updated.
  <li>If apache2 is started, it serves a "Hello World" page on port 80. The service is currently stopped because Flask serves on port 80.
  <li>
</ol>

<h2>Installed Software Packages</h2>
<ol>
  <li>apache2 (stopped, because Flask is running on port 80)
  <li>postgresql (9.3)
  <li>git
  <li>python-pip
  <li>postgresql-server-dev-9.3 
  <li>python-dev 
</ol>

<h2>Installed Python Modules</h2>
<ol>
  <li>SQLAlchemy
  <li>Flask
  <li>oauth2client
  <li>google-api-python-client (not needed)
  <li>psycopg2
</ol>

<h2>Catalog App</h2>
Catalog App (developed in a previous project) is running using web-server Flask an database Postgresql. The sources can be found in /root/CatalogApp.
