pipeline{
    agent {
        docker{
            image 'postman/newman:latest'
        }
    }
    stages{
        
        stage("Vérification newman"){
            steps{
                sh'newman --version'
            }
        }

        stage("Lancement du test"){
            steps{
                sh'newman run collection.json -e preprod.json'  
            }
        }
    }
}