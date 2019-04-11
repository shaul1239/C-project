node {
    stage('version check') {
        sh '''
       export PATH="/opt/cmake/cmake/bin:$PATH"
       cmake --version
         '''
    }
    stage('cloning a project'){
    checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: 'github', url: 'https://github.com/mrsarm/helloworld-c.git']]])
     }   
     stage('Build'){
         sh '''
         export PATH="/opt/cmake/cmake/bin:$PATH"
         cmake --version
         cmake .
         ls
         make
         '''
         
     }
}
http://derekmolloy.ie/hello-world-introductions-to-cmake/

install CMAKE plugin.
