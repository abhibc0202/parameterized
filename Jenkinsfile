pipeline {
agent none;
  parameters {
  booleanParam defaultValue: true, name: 'status'
}
  stages {
    stage ('BUILD') {
      agent {
  label 'label1'
}
      steps {
        parameters {
  string defaultValue: 'build', name: 'name of the stage'
}
        echo " this is build stage "
        git credentialsId: 'mysore', url: 'https://github.com/abhibc0202/java1.git'
      }
    }
    stage ('TEST') {
      agent {
  label 'label2'
}
      steps {
        echo "this is test stage"
        sh "sleep 5"
      }
    } 
     
    stage ('DEPLOY') {
             agent {
  label 'master'
} 
      steps {
        echo "this is deploy stage "
        sh "sleep 5"
      }
    }
  }
}
