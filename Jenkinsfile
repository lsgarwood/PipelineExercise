pipeline {
    agent any
    stages {
        stage('Clone PipelineExercise2') {
            steps {
              git branch: 'main', url: 'https://github.com/lsgarwood/PipelineExercise2.git/'
            }
        }
        stage('Run Script') {
            steps {
                sh 'sh ./myscript'
            }
        }
        stage('Archive Artifacts') {
            steps {
                archiveArtifacts artifacts: 'output', followSymlinks: false
            }
        }
    }
}
