releaseBranch = 'release'
configBranch = '*/master'

pipeline{
    agent any 
    stages{
        stage("Build"){
            when {
                not {
                    branch releaseBranch
                }
                not {
                    branch configBranch
                }
            } 
            steps{
                echo "This is Build stage"
                echo "Build stage is completed successfully -  check release"        
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
                echo "objective is to skip above 2 stages test3 for release branch"
            }
        }
    }
}
