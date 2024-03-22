node {
   stage('Cont.Download') {
   git branch: 'qa', url: 'https://github.com/naga457/newproj.git'
   }
   stage('Cont.Build') {					  
	sh 'mvn clean package'
			  }
	stage('Cont.Deploy') {		  
	deploy adapters: [tomcat9(credentialsId: '3be358fa-552c-432c-9476-170a9e88cf28', path: '', url: 'http://172.31.46.151:8080')], contextPath: '/qa', war: '**/*.war'	}		  
     }
