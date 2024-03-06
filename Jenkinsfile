pipeline {
  agent any
  stages{
     stage('Build') {
            steps {
                build 'PES1UG21CS153-2'
                sh 'g++ hello.cpp -o output'
              }
          }
      stage('Test') {
          steps {
                bnh'./output'
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
