releaseBranch = 'release'
configBranch = '*/master'
all-master = 'all-reals-from-ht3'
all-release = 'all-release-from-ht3'

pipeline{
    agent any 
    stages{
        stage("update chart versions"){
            when {
                expression { BRANCH_NAME ==~ all-master }
//                not {
//                    branch releaseBranch
//                }
            } 
            steps{
                echo "This is Build stage - testing master"
                echo "Build stage is completed successfully"
            }
        }
        stage("verify helm charts"){
//            when { anyOf { branch configBranch; branch releaseBranch } }
            when { expression { BRANCH_NAME ==~ all-master } }
            steps{
                echo "deploy is running - hotfix is done check"
            }
        }
        stage("update image tags"){
            steps{
                when { expression { BRANCH_NAME ==~ all-release } }
                echo "building 3rd stage"
                echo "objective is to skip above 2 stages test3 for release branch"
            }
        }
        stage("for other branches"){
            steps{
                echo "all the other branches are able to run this stage"
                echo "for other branches this stage is build successful"
    }
}
