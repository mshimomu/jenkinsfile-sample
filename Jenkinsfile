node {
  stage 'main'
  git url: 'https://github.com/mshimomu/jenkinsfile-sample.git'
  sh './gradlew clean test'
  step([$class: 'ArtifactArchiver', artifacts: 'build/test-results/*.xml', fingerprint: true])
  step([$class: 'JUnitResultArchiver', testResults: 'build/test-results/*.xml'])
}