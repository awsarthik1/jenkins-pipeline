pipeline{
    agent any 
    stages{
        stage("Build"){
           // when { not { branch1 == 'master' } }
            steps{
                echo "This is Build stage"
                echo "Build stage is completed successfully"        
            }
        }
        stage("Deploy"){
            steps{
                echo "deploy is running"
            }
        }
        stage("3rd stage"){
            steps{
                echo "building 3rd stage"
                echo "objective is to skip above 2 stages test1"
            }
        }
    }
}
