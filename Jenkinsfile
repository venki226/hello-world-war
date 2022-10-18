pipeline { 
    agent { label 'slave3' } 
    stages { 
        stage ('Checkout') 
        { 
            steps {
                sh "pwd"
                sh "rm -rf hello-world-war"
                sh "git clone https://github.com/venki226/hello-world-war.git"
            }
        }
        stage ('Build') 
        { 
             steps {
                sh "ls"
                 sh "cd hello-world-war"
                 sh "mvn clean package"
             }
        }
        stage ('Deploy') 
        { 
             steps {
                sh "cp /home/slave3/workspace/hellowrldtomcat/target/hello-world-war-1.0.0.war /opt/tomcat/webapps"
             }
        }
       }
      }           
