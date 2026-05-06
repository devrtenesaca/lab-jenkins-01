pipeline{
    agent any
    environment {
        NAME = "Jenkins"
        MACHINE = "linux"
    }
    stages{
        stage("checkout"){
            steps{
                echo "========executing A========"
                git branch: 'master', url: 'https://github.com/devrtenesaca/lab-jenkins-01.git'
            }
        }
        stage("build"){
            steps{
                echo "========executing B========"
                sh 'python3 machine.py ${NAME}, ${MACHINE}'
               
            }
        }
   
    }   
}

