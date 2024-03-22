node {
   stage('Cont.Download') {
   git branch: 'test', url: 'https://github.com/naga457/newproj.git'
   }
   stage('Cont.Build') {					  
	sh 'mvn clean package'
			  }
	stage('Cont.Deploy') {		  
	deploy adapters: [tomcat9(credentialsId: '4935e5f9-35c4-4b27-b413-26ca3b77ceee', path: '', url: 'http://172.31.43.122:8080')], contextPath: '/testapp', war: '**/*.war'
	}		  
     }
