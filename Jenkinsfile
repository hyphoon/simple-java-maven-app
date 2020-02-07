pipeline {
	agent {
		docker {
			image 'maven:3-alpine'
			args '-v /c/Usres/Hyphoon/.me2:/root/.m2 --engine-registry-mirror=https://5h0epy64.mirror.aliyuncs.com'
		}
	}
	stages {
		stage('Build') {
			steps {
				sh 'mvn -B -DskipTests clean package'
			}
		}
	}
}