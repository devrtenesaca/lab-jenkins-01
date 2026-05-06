pipeline{
    agent any
    environment {
        NAME = "Jenkins"
        MACHINE = """${
        sh (returnStdout: true, script: 'uname -a').trim()
     }"""
    }
    stages{
        stage("checkout"){
            steps{
                echo "========executing A========"
                git branch: 'master', url: 'https://github.com/devrtenesaca/lab-jenkins-01.git'
                //interpolation variables 
                echo "NAME: ${NAME}"
                echo "MACHINE: ${MACHINE}"
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

