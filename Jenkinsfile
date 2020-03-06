pipeline {
    agent any

    stages {
        stage('mystagename') {
            parallel {
                // One or more stages need to be included within the parallel block.
                stage('clearlinux') {
                    agent {
                        docker {
                            image 'clearlinux'
                        }
                    }
                    steps {
                        sh 'cat /etc/os-release'
                    }
                }

                stage('ubuntu') {
                    agent {
                        docker {
                            image 'ubuntu'
                        }
                    }
                    steps {
                        sh 'cat /etc/os-release'
                    }
                }
            }
        }
    }
}
