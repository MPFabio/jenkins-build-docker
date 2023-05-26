node {
  def app

    stage('clone') {
	checkout scm
    }

    stage('build image') {
	app = docker.build("fabio/nginx")
    }

    stage('run image') {
	docker.image('fabio/nginx').withRun('-p 80:80') { c ->

	sh 'docker ps'
	
	sh 'curl localhost'
  
    }

    }

}
