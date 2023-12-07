pipeline{
	agent any 
	stages{
		stage('1-clonecode'){
			steps{
				checkout scmGit(branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[credentialsId: 'github-creds', url: 'https://github.com/etechteam6/demojenk2.git']])
			}
		}
		stage('2-s2'){
			steps{
				sh 'du -h'
			}
		}
		stage('3-s3'){
			steps{
				echo "my life"
			}
		}
		stage('4-s4'){
			steps{
				echo "this is my life you decide yours!"
			}
		}
        stage('5-s5'){
			parallel{
				stage('p1'){
					steps{
						echo "first parallel job"
					}
				}
				stage('p2'){
					steps{
						echo "we go do am las las"
					}
				}
			}
        }
	}
}