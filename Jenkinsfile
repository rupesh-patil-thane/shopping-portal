pipeline{

    agent any


    tools{
       nodejs 'nodejs'
    }
    

    stages{
        stage('build'){
            steps{
                echo 'this is build the app job'
                sh 'npm install'
            }
        }
        stage('test'){
            steps{
                echo 'this is test the app job'
                sh 'npm test'
            }
        }
        stage('package'){
            steps{
                echo 'this is package the app job'
                sh 'npm run package'
            }
        }
    }
    
    post{
        always{
            echo 'This pipeline has completed...'
        }
        
    }
    
}
