pipeline {
  agent any
  stages{
     stage('Build') {
            steps {
                build 'PES1UG21CS153-1'
                sh 'g++ main.cpp -o output'
              }
          }
      stage('Test') {
          steps {
                bnh './output'
            }
        }
      stage('Deploy') {
          steps {
              echo 'deploy'
            }
        }
    }
    post{
        failure{
            error 'Pipeline failed'

        }
    }
}
