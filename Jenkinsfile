def company='puzzle'

properties([
    buildDiscarder(logRotator(numToKeepStr: '5')),
    pipelineTriggers([
        pollSCM('H/5 * * * *'),
        cron('@midnight')
    ])
])

timestamps() {
    timeout(time: 10, unit: 'MINUTES') {
        node {
            stage('Interpolation') {
                echo 'join the ${company}'
                echo "join the ${company}"
                echo '''join the ${company}'''
                echo """join the ${company}"""
            }
            stage('Environment') {
                echo "Running ${env.BUILD_ID} on ${env.JENKINS_URL} in company ${company}"
            }
            stage('Shell') {
                sh "echo \"${company}\""
                sh "echo \"Running ${env.BUILD_ID} on ${env.JENKINS_URL}\" in company ${company}"
            }
        }
    }
}

