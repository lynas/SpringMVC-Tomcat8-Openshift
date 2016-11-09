## Deploy Spring MVC application on OpenShift in Tomcat 8 server ##

# Command to run app

```
rhc app create demo diy
```

```
git remote add upstream https://github.com/lynas/SpringMVC-Tomcat8-Openshift.git
git pull -s recursive -X theirs upstream master
```
If you get an error saying ```fatal: refusing to merge unrelated histories``` use
```
git pull -s recursive -X theirs upstream master --allow-unrelated-histories
```

```
git push
```

