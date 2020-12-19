pipeline {
    agent any
    parameters{
        choice(name:'VERSION', choices:['1','2','3'], description:'Which version to run')
    }
    stages {
        stage('Build') {
            when{
                expression{params.VERSION == '1'} 
            }
            steps {
                echo "you're running version1"
                input('Do you want to proceed') 
                echo 'this is build step'
            }
        }
        stage('test') {
            steps {
                echo 'this is test '
            }
        }
        stage('deploy') {
            steps {
                echo 'this is deploy'
            }
        }
    }
    post{
        success{
            echo'job success'
        }
    }
}
