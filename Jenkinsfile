node {
    try {
        stage('Test') {
            sh 'echo "Fail!"; exit 1'
        }
        echo 'This is uccessful'
    } catch (e) {
        echo 'Error has been caught'

        // Since we're catching the exception in order to report on it,
        // we need to re-throw it, to ensure that the build is marked as failed
        throw e
    } finally {
        def currentResult = currentBuild.result ?: 'SUCCESS'
        if (currentResult == 'UNSTABLE') {
            echo 'This is unstable'
        }

        def previousResult = currentBuild.previousBuild?.result
        if (previousResult != null && previousResult != currentResult) {
            echo 'This is previous resuls'
            echo 'lets see if previous results not equal to currentResult'
        }

        echo 'Need this to always run'
    }
}
