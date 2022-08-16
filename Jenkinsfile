node {
    def app

    stage('Clone repository') {
<<<<<<< HEAD
        /*11aa Cloning the Repository to our Workspace */
=======
        /* Cloning the Repository to our Workspace .... */
>>>>>>> be80488fda7822f8633f82ab06ff3ac4c65198c6
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
