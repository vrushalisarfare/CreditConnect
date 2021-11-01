node{
  stage('SCM Checkout'){
       git 'https://github.com/vrushalisarfare/javaloginapp'
       }
  stage('Compile-Package'){
    def mvnHome = tool name: 'apache-maven-3.8.3-bin/apache-maven-3.8.3' , type: 'maven'
   sh "C:/apache-maven-3.8.3-bin/apache-maven-3.8.3/bin/mvn package"
  }
  
  stage('SonarQube Analysis'){
    def mvnHome = tool name: 'apache-maven-3.8.3-bin/apache-maven-3.8.3', type: 'maven'
    withSonarQubeEnv('sonar-6'){
      sh "C:/apache-maven-3.8.3-bin/apache-maven-3.8.3/bin/mvn package"
     // sh "${mvnHome}/bin/mvn sonar:sonar"
    }
  }
       }
    
