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
                def company = 'puzzle'
                echo 'join the ${company}'
                echo "join the ${company}"
                echo '''join the ${company}'''
                echo """join the ${company}"""
            }
        }
    }
}
