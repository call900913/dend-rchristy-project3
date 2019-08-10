pipeline {
    agent any
    stages {
        stage('Lint html') {
            steps {
                sh 'tidy -q -e *.html'
            }
        }
        stage('Upload to AWS') {
            steps {
                withAWS(credentials:'aws_static') {
                    s3Upload(file:'index.html', bucket:'jenkinsbucket6632', path:'index.html')
                }
            }
        }
    }
}
