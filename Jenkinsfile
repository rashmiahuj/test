pipeline{
  agent any
  stages{
    stage("run frontend"){
      steps{
        echo "M2_HOME = ${M2_HOME}"
      }
    }
    stage("run backend"){
      steps{
        echo 'executing maven'
        sh 'mvn --version'
      }
    }
  }
}
