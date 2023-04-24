pipeline {
    agent any
    
     options {
  buildDiscarder logRotator(artifactDaysToKeepStr: '10', artifactNumToKeepStr: '', daysToKeepStr: '10', numToKeepStr: '10')

  timestamps()
  
  timeout(time: 12, unit: 'HOURS')
}


triggers{ 
cron('H(0-29)/10 * * * *') 
}

    stages {
        stage('Requirments') {
            steps {
                echo 'This is for requirments'
            }
        }
    }
}
stages {
        stage('Build') {
            steps {
                echo 'This is For build stage'
            }
        }
         stage('test') {
         
            steps {
                echo 'This is testing'
            }
        }
        
         stage('Report') {
         
            steps {
                echo 'This is Reporting'
            }
        }
    
}

post {
  always {
    // One or more steps need to be included within each condition's block.
    echo "This will always run"
  }
}

    
    
