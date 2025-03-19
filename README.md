# linux-tomcat-config

```

sudo vi server.xml



    <Connector port="1111" protocol="HTTP/1.1"
               connectionTimeout="20000"
               redirectPort="1234"
            URIEncoding="UTF-8"/>


    <Host name="localhost"  appBase="webapps"
          unpackWARs="true" autoDeploy="true" deployIgnore=".*">

      <Valve className="org.apache.catalina.valves.AccessLogValve" directory="logs"
             prefix="localhost_access_log" suffix=".txt"
             pattern="%h %l %u %t &quot;%r&quot; %s %b" />
      <Context path="" docBase="/home/ubuntu/web" reloadable="true"/>
    </Host>

    <Host name="domain"  appBase="/path"
            unpackWARs="true" autoDeploy="true">

      <Valve className="org.apache.catalina.valves.AccessLogValve" directory="logs"
             prefix="localhost_access_api_log" suffix=".txt"
              pattern="%h %l %u %t &quot;%r&quot; %s %b" />
    </Host>
    
