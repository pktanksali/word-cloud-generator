node {
//  def exists = fileExists '${WORKSPACE}/src/github.com/pktanksali/word-cloud-generator'
//  if (!exists) {
//    new File('${WORKSPACE}/src/github.com/pktanksali/word-cloud-generator').mkdir()
//  }
  stage('Get code from SCM') {
//    dir('${WORKSPACE}/src/github.com/pktanksali/word-cloud-generator') {
      checkout changelog: false, poll: false, scm: [$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], subdir: '${WORKSPACE}/src/github.com/pktanksali/word-cloud-generator', userRemoteConfigs: [[url: 'https://github.com/pktanksali/learning-iac.git']]]
//    }
  }
  stage('Cleanup') {
    cleanWs()
  }
}

