pipeline {
    agent any 

    stages {
        stage('Build') { 
            steps { 
                bat 'echo Build Job completed sucessfully'
            }
        }
        stage('Test'){
            steps {
                bat 'echo Test job completed sucessfully'  
            }
        }
        stage('Deploy') {
            steps {
                bat 'echo Deploy job completed successfully'
            }
        }
    }
    post{
        always{
            bat 'echo This will aways run'
        }
        sucsess{
            bat 'echo This will run only when job is sucessful'
        }
        failure{
            bat 'echo This will run only when job is failed'
        }
    }

}
