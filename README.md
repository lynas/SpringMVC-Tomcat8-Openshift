## Run Spring MVC application on Apache Tomcat 8 on OpenShift ##

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

rhc ssh demo
cd $OPENSHIFT_DATA_DIR
./tomcat8/bin/shutdown.sh
rm -rf tomcat8/webapps/ROOT
./tomcat8/bin/startup.sh

exit


```

