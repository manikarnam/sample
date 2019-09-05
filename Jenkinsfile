pipeline {
    agent { label 'slave_node' }

      stages {
         stage ('Build && push'){
             steps {
                 script{
               checkout scm

                 docker.withRegistry('https://registry.hub.docker.com', 'dockerhub') {

                 def customImage = docker.build("maniengg/techng")
                     .withRun('-p 80:80','nginx') {
                   
                  // customImage.push()
                  //  customImage.pull()
                                  
                  }   
                }
              }
            }
         }
     }
}
