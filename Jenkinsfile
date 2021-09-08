@Library('piper-lib-os@v2.30.2') _
node() {
    stage('prepare') {
        checkout scm
        setupCommonPipelineEnvironment script:this
    }
  stage('build') {
    mtaBuild script: this
    }
    
    stage('deploy') {
    cloudFoundryDeploy script: this
    }
  
}
