node {

  properties([
    pipelineTriggers([
      foo('test')
    ])
  ])

  stage('Build') {
    sh 'echo "Hey!"'
  }
  stage('Test') {
    sh 'echo "Test!"'
  }
}

def foo(String proj) {
  upstream(
    threshold: hudson.model.Result.SUCCESS,
    upstreamProjects: "${proj}/${BRANCH_NAME}"
  )
}
