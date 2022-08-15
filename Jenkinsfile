node {
    def app


    stage('Clone repository'){

    	checkout scm 
    }
    

    stage('Build image') {
        /* This builds the actual image */

        app = docker.build("forteu/web-app")
    }
  
   stage('Test imgae'){
    
   app.inside{
	echo "App is running" 
	}

  }
