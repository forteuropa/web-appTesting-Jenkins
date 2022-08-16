node {
    def app

    stage('Clone repository') {
        /* Cloning the Repository to our Workspace ....11 */
        checkout scm
    }

    stage('Build image') {
        /* This builds the actual image */

        app = docker.build("forteuropaa/web-app")
    }
    stage('Push image') {
      
        docker.withRegistry('https://registry.hub.docker.com', 'dockerHub') {
            app.push("${env.BUILD_NUMBER}")
            app.push("latest")
            } 
                echo "Trying to Push Docker Build to DockerHub"
    }

}
