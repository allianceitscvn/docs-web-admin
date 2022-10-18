# Jenkins Gitlab

## Summary

* Chose type of trigger in Jenkins
* Create web hook trigger  in Gitlab
* Open port/add whitelist connection from gitlab to jenkins
* Trigger chat/email when jenkins finish

## Jenkins - build trigger

### Trigger builds remotely

![](<../../.gitbook/assets/image (3).png>)

## Gitlab - create web hook

![](<../../.gitbook/assets/image (2) (2).png>)

## Whitelist gitlab

GitLab.com uses the IP ranges `34.74.90.64/28` and `34.74.226.0/24` for traffic from its Web/API fleet

{% embed url="https://docs.gitlab.com/ee/user/gitlab_com/" %}



## Issues

### No authenticator

```
// Some codeHook executed successfully but returned HTTP 403 <html> <head> <meta http-equiv="Content-Type" content="text/html;charset=ISO-8859-1"/> <title>Error 403 No valid crumb was included in the request</title> </head> <body><h2>HTTP ERROR 403 No valid crumb was included in the request</h2> <table> <tr><th>URI:</th><td>/job/NotifyService/build</td></tr> <tr><th>STATUS:</th><td>403</td></tr> <tr><th>MESSAGE:</th><td>No valid crumb was included in the request</td></tr> <tr><th>SERVLET:</th><td>Stapler</td></tr> </table> <hr/><a href="https://eclipse.org/jetty">Powered by Jetty:// 9.4.45.v20220203</a><hr/> </body> </html>
```

Resolve

Add username and token user of Jenkins to url

Example: [http://user:token@url:8080/job/Project/build?token=Token](http://user:token@url:8080/job/Project/build?token=Token)



