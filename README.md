Note:
====

jenkins by default runs with jenkins user on the linux box, so this pipeline executed on the jenkins server with user jenkins.

Before making this work, you might need to have git & terraform installed on the jenkins server possibly you should be able to execute terraform and git commands work as a jenkins user on the jenkins server.

As this is just an example, I thought it doesn't have to follow best practices

Usage:
------
1. update vars.tf with your access/secret keys
2. make sure terraform and git commands working on the server manually
3. follow the tutorial

I have updated the repo with ReadMe and also with vars.tf to make it more sense as more people pinging me and asking me in detail. Hope this readme would throw some insight. 


Improvements:
------------

You can use below commands to plan and apply terraform. You can have them in different stages within Jenkinsfile

$ terraform plan
$ terraform apply -auto-approve

Once this is successful at any time if you want to remove the provisioned instance. Execute below command on the jenkins server as jenkins user

$ terraform destroy -auto-approve

#Cheers - Pavan Kumar Aleti
