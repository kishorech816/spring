pipeline {
    agent any
        stages {
                  stage("Checkout") {
                      steps {
                    git changelog: false, credentialsId: '56e8cd48-9cc0-4488-8b03-260e52854a72', poll: false, url: 'https://github.com/kishorech816/spring.git'
                  }
                 } 
                stage('Compile & build') {
            //agent { label 'master'}
                    steps {
                    bat label: '', script: 'mvn clean'
                    //sh 'mvn clean package'
                    //stash name:"war", includes:"*/*.war"
            }
        }
        }      
 }
