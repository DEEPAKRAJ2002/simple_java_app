pipeline {
  agent any
  
  stages {
    stage ("Git Checkout") {
      steps {
        git branch: "main", url: "https://github.com/DEEPAKRAJ2002/simple_java_app.git"
      }
    }
    
    stage ("Build") {
      steps {
        sh "mvn clean package"
      }
    }
    
    stage ("Deploy") {
      steps {
        sh "java -jar target/myapp-1.0-SNAPSHOT.jar" 
      }
    }   
  }
}
