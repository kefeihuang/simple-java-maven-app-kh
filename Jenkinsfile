pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
//                 powershell 'mvn -B -DskipTests clean package'
                script {
                    if (isUnix()) {
                        echo "Running on a Linux/Unix-based agent"
                        sh 'uname -a'
                    } else {
                        echo "Running on a Windows-based agent"
                        bat 'ver'
                    }
                    sh 'mvn -B -DskipTests clean package'
                }
            }
        }
    }
}
