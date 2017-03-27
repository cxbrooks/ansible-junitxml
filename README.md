ansible-junitxml
================

``ansible-junitxml`` is a shell script that reads [Ansible IT automation](https://www.ansible.com) playbook output from a file and generates JUnit XML results on standard out for use in the [Jenkins continuous integration system](https://jenkins.io).

To use this in Jenkins, in the Build section of the configuration, add a "Execute Shell" section with a command that invokes the script on the Ansible output.

```
mkdir -p $WORKSPACE/reports
~/src/swarmboxadmin/ansible/bin/ansible2JUnixXML $JENKINS_HOME/jobs/swarmboxadmin/builds/$BUILD_NUMBER/log > $WORKSPACE/reports/ansibleJUnit.xml
```



