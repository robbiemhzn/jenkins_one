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
		     sh 'docker run -dit --name httptst02 -p81:80 httptst'
		     }
		}
}
}
