pipeline
{

    agent any
    stages
    {

        stage('scm checkout')
        {
            steps {git branch: 'master', url: 'https://github.com/Vishal6747/maven-project.git'}
        }
        stage('run unit test framework')
        {
            steps{
                withMaven(jdk: 'JAVA_HOME', maven: 'MVN_HOME') {
                    sh 'mvn test'
            }
            }
        }
        stage('deploy package')
        {
           steps
           {
               withMaven(jdk: 'JAVA_HOME', maven: 'MVN_HOME') {
                    sh 'mvn package'
            }
           } 
        }
    }
}