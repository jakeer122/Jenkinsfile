pipeline {
    agent { docker { image 'golang:1.14' } }
    tools {
        go 'go-1.11'
    }    
    environment {
        GOCACHE = '/tmp/gocache'
        GO111MODULE = 'on'
    }
    stages {
        stage('build') {
            steps {
                sh 'go build'
            }
        }
        stage('test') {
            steps {
                sh 'go test ./...'
            }
        }
    }
}
