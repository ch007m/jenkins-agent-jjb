# jenkins-agent-jjb

To build the image on openshift, execute the following command

```bash
oc delete is,buildconfig jenkins-agent-jjb -n ci-cd
oc -n ci-cd apply -f https://raw.githubusercontent.com/ch007m/jenkins-agent-jjb/main/openshift/is.yml
oc -n ci-cd apply -f https://raw.githubusercontent.com/ch007m/jenkins-agent-jjb/main/openshift/bc.yml
oc start-build jenkins-agent-jjb -n ci-cd
```