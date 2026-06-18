pipeline{

agent any
tools{
gradle 'Gradle'
jdk 'JDK'
}

stages{
stage ('Checkout'){
steps{
git url:'https://github.com/vs-vanshika/MyGradleApp.git'
}
}
stage ('Build')
{
steps{
sh 'gradle build'
}
}

stage ('Test'){
steps{
sh 'gradle test'
}
}

stage ('Run'){
steps{
sh 'gradle run'
}
}
}

post{
success{
echo 'Build Success'
}
failure{
echo 'Build failure'
}
}
}
