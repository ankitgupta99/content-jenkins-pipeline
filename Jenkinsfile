pipeline {
 agent any
 stages {
 stage('build') {
 steps {
 sh '/var/lib/jenkins/jdk-10.0.2/bin/javac -d . src/*.java'
 sh 'echo Main-Class: Rectangulator > MANIFEST.MF'
 sh 'jar -cvmf MANIFEST.MF rectangle.jar *.class'
 }
 }
 }
}
