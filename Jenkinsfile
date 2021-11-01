node{
  stage('SCM Checkout'){
       git 'https://github.com/vrushalisarfare/javaloginapp'
       }
  stage('Compile-Package'){
    def mvnHome = tool name: 'apache-maven-3.8.3' , type: 'maven'
    sh "${mvnHome}/bin/mvn package"
  }
  
  stage('SonarQube Analysis'){
    def mvnHome = tool name: 'apache-maven-3.8.3', type: 'maven'
    withSonarQubeEnv('sonar-6'){
      sh "${mvnHome}/bin/mvn sonar:sonar"
    }
  }
       }
    
