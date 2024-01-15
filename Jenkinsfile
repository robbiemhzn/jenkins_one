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
		     sh 'docker run -dit --name httptst05 -p83:80 httptst'
		     }
		}
}
}
