# Jenkins Pipeline

## Cơ bản

```groovy
pipeline {
    agent any
    stages { 
        stage('Clone') {
            //implement pipeline code 
        }
        stage('Build') {
            //implement pipeline code 
        }
        stage('Test') {
            //implement pipeline code 
        }
    }
}
```

## Test for windows server

```
#!/usr/bin/env groovy

def changeCount = 0
def googleChatHook = "https://chat.googleapis.com/v1/spaces/AAAAuWV60uo/messages?key=AIzaSyDdI0hCZtE6vySjMm-WEfRq3CPzqKqqsHI&token=-mKv2hAVHBIw9DdEMRj23TaO2xJ-iRnJ_kqqlCumjTQ%3D"

pipeline {
    agent any
    stages {
      stage('Check shell') {
        steps {
          echo "Check Shell: ${env.JOB_NAME}"
          bat 'java --version'
          bat 'node --version'
          bat 'echo %USERNAME%'
          bat 'echo %CD%'
          script {
            changeCount = currentBuild.changeSets.size()            
            echo "${changeCount} commit(s) since last buid." 
          }
        }
      }          
    }    
    post{
        success{
          echo "POST Success"
          googlechatnotification (
            url: googleChatHook,
            message: "Test post success"
          )
        } 
        unsuccessful{
          echo "POST Failed"
          googlechatnotification (
            url: googleChatHook,
            message: "Test post failed"
          )
        }    
    }
}

```

