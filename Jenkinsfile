
pipeline{
    agent any

    stages{

        stage('Checkout') {
            steps{
                git branch: 'main',
                    url: 'http://192.168.0.121:7990/scm/jen/test-yamlllint.git'
                sh "pwd"
            }
        }


        stage('Testing') {
            steps {
              sh "cat test.yaml"
                script {
                     OUTPUT = sh (
                        script: "yamllint test.yaml",
                        returnStdout: true
                    ).trim()
                    print(OUTPUT)
                }
            }
        }

    }
}
