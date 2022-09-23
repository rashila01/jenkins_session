pipeline{
    agent any
    stages{
        stage("Basic Setup"){
            steps{
                echo "Basic setup Start"
                bat "yarn install"
                echo "Basic setup completed"
            }
        }
// here the actual automation is ran.
        stage("Ru Automated Tests"){
            parallel{
                stage("CI Machine #1") {
                    steps {
                        bat "yarn cypress run --parallel --record --key=e4d5b964-9cb5-46d6-bbc4-60f7f295689c --ci-build-id 3 --group rashila_parallelrun"
                    }
                }
                stage("CI Machine #2") {
                    steps {
                        bat "yarn cypress run --parallel --record --key=e4d5b964-9cb5-46d6-bbc4-60f7f295689c --ci-build-id 3 --group rashila_parallelrun"
                    }
                }
                stage("CI Machine #3") {
                    steps {
                        bat "yarn cypress run --parallel --record --key=e4d5b964-9cb5-46d6-bbc4-60f7f295689c --ci-build-id 3 --group rashila_parallelrun"
                    }
                }
            }
        }
        stage("Report Generation"){
            steps{
                echo "Report Generation Process Running"
            }
        }
        //remove unnecessary files
        stage("Remove unnecessary files"){
            steps{
                echo "Remove unnecessary files"
            }
        }
    }
}

//steps{
                // echo "Basic setup Start"
                // bat "yarn install"
                // echo "Basic setup completed"
            // }