node {

  properties([
    pipelineTriggers([
      upstream(
        threshold: hudson.model.Result.SUCCESS,
        upstreamProjects: "test/${BRANCH_NAME}"
      )
    ])
  ])

  stage('Build') {
    sh 'echo "Hey!"'
  }
  stage('Test') {
    sh 'echo "Test!"'
  }
}
