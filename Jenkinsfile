node {
  stage ('SCM Checkout'){
  
  git  credentialsId: 'ja81',
       url: 'git@github.com:ja81/Quarkus-Rest.git'
  }
  
  stage ('Compile-Package'){
  dev mvnHome = tool name: 'maven-3', type: 'maven'
    sh "${mvnHome}/bin/mvn package -Pnative -Dquarkus.native.container-build=true"
  }
 }
