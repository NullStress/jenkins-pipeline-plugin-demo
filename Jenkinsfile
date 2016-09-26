node {
    currentBuild.result = "SUCCESS"

    try {

        stage 'Checkout'

        checkout scm

        stage 'Test'

        sh 'chmod +x gradlew'
        sh './gradlew clean build'
    }
    catch (err) {

        currentBuild.result = "FAILURE"


        throw err
    }
}