node {
    stage('checkout scm'){
    git 'https://github.com/Babita-123/simple-java-maven-app.git'
    }
    
    stage('SonarQube analysis') {
    withSonarQubeEnv('sonar-6') {
    sh 'mvn org.sonarsource.scanner.maven:sonar-maven-plugin:3.6.0.1398:sonar'
    } // submitted SonarQube taskId is automatically attached to the pipeline context
  }
        
    stage('Compile-Package'){
    sh 'mvn package'
    }
}
    
