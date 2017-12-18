pipeline {
    agent any 
    currentBuild.result= "SUCCESS"
    try{
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
                    mail body: 'Project build completed sucessfully',
                            from: 'sagar.chavan.ext@siemens.com',
                            replyTo:'sagar.chavan.ext@siemens.com',
                            subject: 'Deploy completed',
                            to: 'sagar.chavan.ext@siemens.com'
                }
            }
        }
        post{
            always{
                bat 'echo This will aways run'
            }   
            success{
                bat 'echo This will run only when job is sucessful'
            }
            failure{
                bat 'echo This will run only when job is failed'
            }
        }
    }
    catch(err){
        currentBuild.result= "FAILURE"
        throw err
    }
}
