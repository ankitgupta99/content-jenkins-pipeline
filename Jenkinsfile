pipeline {
 agent any
 stages {
 stage('build') {
 steps {
 sh '/var/lib/jenkins/jdk-10.0.2/bin/javac -d . src/*.java'
 sh 'echo Main-Class: Rectangulator > MANIFEST.MF'
 sh '/var/lib/jenkins/jdk-10.0.2/bin/jar -cvmf MANIFEST.MF rectangle.jar *.class'
 }
 }
 stage('approval test') {
 steps {
 sh '/var/lib/jenkins/jdk-10.0.2/bin/javac -d . src/*.java'
 input "Deploy to pr?"
 }
 }
stage('run') {
 steps {
 sh '/var/lib/jenkins/jdk-10.0.2/bin/java -jar rectangle.jar 7 9'
 }
 }
 
}
}
