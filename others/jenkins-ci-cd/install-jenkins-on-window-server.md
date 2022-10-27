# Install Jenkins on Window Server

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
