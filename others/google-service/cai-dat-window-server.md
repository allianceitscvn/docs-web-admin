# Cài đặt window server

## Create new google cloud - windows server

* Chose windows server
* After created, create RDP password for user
* Add IP statics (options)
* Add network firewall: 8080, 8888 v.v...

## Step first init windows server

* Remote windows server
* Install 7zip
* Install jenkins (options)
  * Install jdk 11
  * Install git scm
* Install nodejs 14 (options)
  * npm install --global yarn
  * npm install -g env-cmd
* Install IIS
  * Enable-iis-2022-components-server:
    * Open Server Manager and click Manage > Add Roles and Features. Click Next to install IIS
  * Install URL-rewrite : https://www.iis.net/downloads/microsoft/url-rewrite
  * Install IIS ARR: https://www.iis.net/downloads/microsoft/application-request-routing
  * Install Dotnet (https://dotnet.microsoft.com/en-us/download/dotnet/5.0)
    * Install dotnet SDK (options for build)
    * Install dotnet runtime
* Add firewall inboud
  * Port 8080, 9090 for jenkins
  * Port 8888 for web test
  * Port 5000-5100 for ftp

## Install FTP Site

* Follow: https://winscp.net/eng/docs/guide\_windows\_ftps\_server
* Port chanel: 5000-5100
* Create self certificate for FTP-Server
* Open firewall: 5000-5100
* Add FTP Site with port 21

## Intall Jenkins

* Follow install jenkins tutor
* Open localhost:8080 for first setup
* Enable proxy compatibility in Configure Security
* Install plugins svn
* Install plugins google chat
*   Add site jenkins

    * Add site jenkins port 9090
    * Enable proxy
    * Edit web.config

    ```
    <?xml version="1.0" encoding="utf-8"?>
    <configuration>
        <system.webServer>
            <rewrite>
                <rules>
                    <rule name="Reverse Proxy to Jenkins" stopProcessing="true">
                        <match url="(.*)" />
                        <action type="Rewrite" url="http://localhost:8080/{R:1}" />
                    </rule>
                </rules>
            </rewrite>
        </system.webServer>
    </configuration>
    ```
* Add project Test with pipeline test
* Run test finish
