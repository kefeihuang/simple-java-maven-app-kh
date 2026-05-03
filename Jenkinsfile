pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
//                 powershell 'mvn -B -DskipTests clean package'
                if (isUnix()) {
                        echo "Running on a Linux/Unix-based agent"
                        sh 'uname -a'
                    } else {
                        echo "Running on a Windows-based agent"
                        bat 'ver'
                    }
            }
        }
    }
}
