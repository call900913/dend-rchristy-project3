pipeline {
    agent any
    stages {
        steps {
            sh 'echo "Hello World"'
            sh '''
                echo "Multiline shell steps work as well"
                ls -lah
            '''
        }
    }
}
