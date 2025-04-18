pipeline {
agent any
stages {
stage('Clone') {
steps {
echo 'Cloning the repository...'
// Repo already cloned by Jenkins
}
}
stage('Build Docker Image') {
steps {
script {
echo 'Building Docker image...'
dir('node-app') {
bat 'docker build -t node-jenkins-app .'
}
}
}
}
stage('Run Docker Container') {
steps {
script {
node-jenkins-app'
}
}
echo 'Running Docker container...'
bat 'docker run -d --name node-jenkins-container -p 3000:3000
}
}
post {
success {
}
failure {
}
echo 'Pipeline completed successfully.'
echo 'Pipeline failed.'
}
}