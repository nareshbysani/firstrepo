pipeline {
    agent any 
    stages {
        stage('Example Build') {
            steps {
                script {
                 if (!env.gitlabActionType){
      echo "Build triggered by the scan process, Ignore it!"
      currentBuild.result = 'NOT_BUILT'
      error('Aborting build triggered by scan process')
    }   
                }
                
                echo 'Hello, Maven'
                
            }
        }
        stage('Example Test') {
           steps {
                echo 'Hello, JDK'
                
            }
        }
    }
}
