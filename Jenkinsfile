pipeline{

    agent any

    stages{

        stage('Continous Download') {

            steps{
                git branch: 'main', url: 'https://github.com/Hadijah-ateh/NEW-PROJECT-3.git'
            }
        }
        stage("Intergration Testing"){

            steps{
                sh 'mvn verify -DskipUnitTest'
            }
        }
        stage("Unit Test"){

            steps{
                sh 'mvn test'
            }
        }
        stage("Continous Build"){

            steps{
                sh 'mvn clean install'
            }
        }
    }
}