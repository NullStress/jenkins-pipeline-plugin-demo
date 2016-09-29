node {
    currentBuild.result = "SUCCESS"

    try {

        stage 'Checkout'

        checkout scm

        stage 'Test'

        def mavenHome = tool 'M3'
        sh '${mavenHome}/bin/mvn clean install'
    }
    catch (err) {

        currentBuild.result = "FAILURE"


        throw err
    }
}
