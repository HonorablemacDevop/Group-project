pipeline {
    agent any

    stages {
        stage('GIT_SRC_CLONE') {
            steps {
                git branch: 'master', url: 'https://github.com/HonorablemacDevop/Group-project.git'
            }
        } 
        stage('MAVEN_BUILD') {
            steps {
                script{
                def mavenHome = tool name: "maven3.9.4", type "maven"
                def mavenCMD = "${mavenHome}/bin/mvn"
                sh "${mavenCMD} clean package"
            }
        }
    }
}
}
