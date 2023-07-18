node{
    stage('1-BUILD'){
        sh 'rm -rf jenkins'
        git branch: 'main', credentialsId: 'Jenkins', url: 'https://github.com/RPetrosjan/jenkins.git'
    }
    stage('2-RUN'){
        sh 'ls -all'
    }
    stage('3-TEST'){
        sh 'cat me.txt'
    }
    stage('Sonar Scan'){
        withSonarQubeEnv('My SonarQube Server') {
            sh 'mvn clean package sonar:sonar'
        }
    }
    
}
