# jenkins-agent-jjb

To build the image on openshift, execute the following command

```bash
oc delete is,buildconfig jenkins-agent-jjb -n ci-cd
oc -n ci-cd apply -f openshift/
oc start-build jenkins-agent-jjb -n ci-cd
```