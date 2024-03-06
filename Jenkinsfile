pipeline {
    agent any
    
    environment{
        VERSION="1.0"
    }

parameters{
      booleanParam(name: 'TOGGLE', defaultValue: true, description: 'Toggle this value')
}

    stages {
        
        stage('Checkout'){
            steps{
               git url:'https://github.com/tahyd/ml-bc-flaskqpp.git',
                   branch:'master'
                 
            }
        }
        stage('Build') {
            steps {
                echo "${VERSION}"
                echo "${params.TOGGLE}"
            }
        }
        
        // end of the build
        stage("test"){
            steps{
                echo 'Test'
            }
        }
    }
    
    
   post{
       always{
           echo 'aways'
       }
       success{
           echo 'sucess'
       }
       failure {
           echo 'failure'
       }
   } 
}
