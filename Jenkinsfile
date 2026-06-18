pipeline {
agent any // Use any available agent
tools {
gradle 'Gradle'
jdk 'JDK' }
stages {

stage('Build') {
steps {
sh 'gradle build' // Run Gradle build
}
}
stage('Test') {
steps {
sh 'gradle test' // Run unit tests
}
}
stage('Run') {
steps {
sh 'gradle run'
}
}
}
post {
success {
echo 'Build and deployment successful!' }
failure {
echo 'Build failed!' }
}
}
