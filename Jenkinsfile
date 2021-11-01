node{
  stage('SCM Checkout'){
       git 'https://github.com/vrushalisarfare/javaloginapp'
       }
  stage('Build & Package') {
withSonarQubeEnv('sonar-6') {
bat 'mvn clean package sonar:sonar'
}
}
  //stage('Compile-Package'){
    //def mvnHome = tool name: 'apache-maven-3.8.3' , type: 'maven'
      // sh "${mvnHome}/bin/mvn clean package"
   // sh 'mvn clean package sonar:sonar'
 // }
  
 // stage('SonarQube Analysis'){
   // def mvnHome = tool name: 'apache-maven-3.8.3', type: 'maven'
   // withSonarQubeEnv('sonar-6'){
     // sh "${mvnHome}/bin/mvn sonar:sonar"
     // sh 'mvn clean package sonar:sonar'
//    }
//  }
       }
    
