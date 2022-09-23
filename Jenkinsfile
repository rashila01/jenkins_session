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
            pararell{
                stage("CI Machine #1") {
                    steps {
                        bat "yarn cypress run --parallel"
                    }
                }
                stage("CI Machine #2") {
                    steps {
                        bat "yarn cypress run --parallel"
                    }
                }
                stage("CI Machine #3") {
                    steps {
                        bat "yarn cypress run --parallel"
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