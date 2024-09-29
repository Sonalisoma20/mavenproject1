pipeline
{
agent any
stages
{
stage('scm checkout')
  {steps { git branch: 'master', url: 'https://github.com/Sonalisoma20/mavenproject1.git' }}

stage('compile the job')
{steps { withMaven(globalMavenSettingsConfig: '', jdk: 'JDK_devops', maven: 'Maven_devops', mavenSettingsConfig: '', traceability: true) {
    sh 'mvn compile'
}}}

stage('execute unit test framework')
{steps { withMaven(globalMavenSettingsConfig: '', jdk: 'JDK_devops', maven: 'Maven_devops', mavenSettingsConfig: '', traceability: true) {
    sh 'mvn test'
}}}

stage('build the code')
{steps { withMaven(globalMavenSettingsConfig: '', jdk: 'JDK_devops', maven: 'Maven_devops', mavenSettingsConfig: '', traceability: true) {
    sh 'mvn package'
}}}

}
}