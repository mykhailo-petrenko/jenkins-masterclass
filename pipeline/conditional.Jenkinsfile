pipeline {
    agent any

    parameters {
        booleanParam(name: 'DO_CONDITION_1', defaultValue: false, description: 'Run or skip the Conditional stage 1')
    }

    stages {
        stage("Init") {
            steps {
                deleteDir()

                echo "INIT"
            }
        }

        stage("Contition 1") {
            steps {
                echo "BEFORE Script ${params.DO_CONDITION_1}."

                script {
                    if (params.DO_CONDITION_1 == false) {
                        currentBuild.result = "SUCCESS"
                        return
                    } else {
                        echo "Contitional build 1 enabled."
                        echo "Build 1!"
                    }
                }

                echo "AFTER Script ${params.DO_CONDITION_1}."
            }
        }
    }
}