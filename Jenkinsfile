node {
    def app


    checkout scm
    }

    stage('Build image') {
        /* This builds the actual image */

        app = docker.build("anandr72/nodeapp")
    }
