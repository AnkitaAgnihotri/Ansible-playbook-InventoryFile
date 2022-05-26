# Ansible-playbook-inventoryFile
### This repo contains inventory file for connectivity (ssh) with remote machine or same machine.
### configuration file for managing SSH connections and inventory.
### ansible-playbook YAML file (webapp.yml) to install JDK,Tomcat.
### Ansible Roles YAML file
### war file to be deployed on tomcat and tar file to unarchived, install, start tomcat using playbook under ansibleRoles->files
### server.xml file to set port number and configuration for tomcat
### Then this playbook is deployed on jenkins (project->configure->scm->gitRepoPath->build->invokeAnsible->nameofplaybookYaml) to get invoked by jenkins when changes are commited to git/gitea scm from local and build triggered (periodic/pollscm/webhook) to make automated deployment as in DevOps Fashion by using CI-CD pipeline
### source code management can be (git or gitea).
### programmer can also use pre/post build steps (jenkins->project->configure) to use sonar for code quality inspection and testing coverage (system testing by gecko driver selenium)
### and deploy binary artifacts (war/jar) in binary Repository JFROG
### After this artifacts can be deployed on tomcat server to get UI output of webApplication by setting post-Build steps for tomcat under jenkins to make automation end to end. 
### this is automated Deployment from sourceCodeRepo to binaryCodeRepo using CI-CD pipeline using tool :
#### code writing IDE(eclips/intellij)
#### BuildTool(maven)
#### Source Code Management (git/gitea)
#### jenkins (for automation provide CI-CD pipeline by configuring project with scm,build,buildTrigger,pre-buildSteps,post-buildSteps,post-buildActions)
#### storing artifacts in binarySourceCodeRepo (Jfrog)
#### for code quality inspection and test coverage (Sonarqube)
#### server for webApplication Deployment to view (Apache tomcat)
#### To maintain connectivity between remote and local machine and to do automated installation and deployment from one machine to another (one environment to another) using playbook without any need of agent installed in remote machine (only require python2/3) we use ANSIBLE
#### containers (docker/kubernetes) also come in picture for contanerization and orchestration of service
