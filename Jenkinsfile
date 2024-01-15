pipeline {
     agent any

     stages {
         stage ('Build'){
	 	steps{
		sh 'ls -ltr'
		sh 'pwd'
		     echo "i am in build"
		     sh 'cd docker && docker build -t httptst .'
		     sh 'docker image ls | grep httptst'
		     sh 'docker ps -a | grep httptst05 | awk \'{print $1}\' | xargs docker rm -f || true'
		     sh 'docker run -dit --name httptst05 -p83:80 httptst'
		     }
		}
}
}
