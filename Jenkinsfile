pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                script {
                    // Get the current workspace directory
                    def workspaceDir = pwd()
                    
                    // Clone the current Git repository
                    checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[url: "file://${workspaceDir}"]]])
                }
            }
        }
        
        stage('Print Hello World') {
            steps {
                echo 'Hello, world'
            }
        }
    }
}
