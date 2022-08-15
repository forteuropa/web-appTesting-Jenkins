node {
    checkout scm

    def customImage = docker.build("weba-app:${env.forteu}")

    customImage.inside {
        sh 'make test'
    }
}
