pipeline {
      agent any 
      
      stages{
        
             stage ('get Code from SCM'){
                 steps{
                     git 'https://github.com/mm-repo/DevOpsClassCodes'
                 }
             }
                 
                  stage ('CompileJob'){
                 steps{
                   sh ' /var/lib/jenkins/tools/hudson.tasks.Maven_MavenInstallation/mymaven/bin/mvn compile'
                 }
                 }
             
                        stage ('TestJob '){
                 steps {
                   sh ' /var/lib/jenkins/tools/hudson.tasks.Maven_MavenInstallation/mymaven/bin/mvn test'
                 }
                  }
                   
                    stage ('PackagingJob') {
                 steps{
                   sh ' /var/lib/jenkins/tools/hudson.tasks.Maven_MavenInstallation/mymaven/bin/mvn package'
                      }
                    }
      }
} 
