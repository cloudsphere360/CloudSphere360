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

    }
}