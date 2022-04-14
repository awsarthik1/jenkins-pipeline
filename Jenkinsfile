releaseBranch = 'release'
configBranch = '*/master'
allMaster = 'all-reals-from-ht3'
allRelease = 'all-release-from-ht3'

pipeline{
    agent any 
    stages{
        stage("update chart versions"){
            when {
                expression { BRANCH_NAME ==~ allMaster }
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
            when { expression { BRANCH_NAME ==~ allMaster } }
            steps{
                echo "deploy is running - hotfix is done check"
            }
        }
        stage("update image tags"){
            when {
                expression {
                    BRANCH_NAME ==~ releaseBranch
                    BRANCH_NAME ==~ allMaster
                }
             }  
//            when { expression { BRANCH_NAME ==~ /(allMaster|configBranch)/ } }
//            when { expression { BRANCH_NAME ==~ allRelease } }
            steps{
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
    }
}
