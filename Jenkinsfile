node {
   stage('Cont.Download') {
   git branch: 'dev', url: 'https://github.com/naga457/newproject1.git'
   }
   stage('Cont.Build') {					  
	sh 'mvn clean package'
			  }
	stage('Cont.Deploy') {		  
	deploy adapters: [tomcat9(credentialsId: '0ebe0cfc-3c03-4432-91b1-0691686018ab', path: '', url: 'http://172.31.14.244:8080')], contextPath: '/devapp', war: '*/.war'	  
			  }		  
     }
