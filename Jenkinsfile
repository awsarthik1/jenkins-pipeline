releaseBranch = 'release'
configBranch = '*/master'

pipeline{
    agent any 
    stages{
        stage("Build"){
            when { anyOf { branch configBranch; branch releaseBranch } }
            steps{
                echo "This is Build stage - testing master"
                echo "Build stage is completed successfully"
            }
        }
        stage("Deploy"){
            when { anyOf { branch configBranch; branch releaseBranch } }
            steps{
                echo "deploy is running - hotfix is done check 2"
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
