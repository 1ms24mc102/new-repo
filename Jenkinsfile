pipeline{
	agent any
	stages{
		stage("Git Start"){
			step{
				echo "From Git pipeline started"
				git branch:'main',url:"https://github.com/1ms24mc102/new-repo/"
			}
		}
		stage("Git End"){
			step{
				echo "From Git pipeline completed"
			}
		}
		stage("Compiling"){
			step{
				echo "Compiling source code..."
				sh "javac Hello.java"
			}
		}
		stage("Running"){
			step{
				echo "Running unit test..."
				sh "java Hello"
			}
		}
	}
}
