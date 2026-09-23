@Library('jenkins-shared-library') _

pipeline {
    agent {
        label 'Jenkins Server Agent-1'
    }

    stages {

        stage('Checkout CloudSphere360 Repository') {
            steps {
                checkout scm
            }
        }

        stage('Maven Compile & Build Project') {
            steps {
                buildWithMaven()
            }
        }

        stage('Verify Docker Build Context') {
            steps {
                sh '''
                    echo "Current workspace:"
                    pwd

                    echo "Target contents:"
                    ls -lah target/

                    echo "JAR files:"
                    find target -maxdepth 1 -type f -name "*.jar" -print
                '''
            }
        }

        stage('Build The Image With Docker') {
            steps {
                buildDockerImage()
            }
        }
    }
}