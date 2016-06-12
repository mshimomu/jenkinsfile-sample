node {
  stage 'main'
//  git url: 'https://github.com/mshimomu/jenkinsfile-sample.git'
  checkout scm
  sh './gradlew clean test'
  step([$class: 'ArtifactArchiver', artifacts: 'build/test-results/*.xml', fingerprint: true])
  step([$class: 'JUnitResultArchiver', testResults: 'build/test-results/*.xml'])
}