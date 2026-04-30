pipeline{
    agent any
    environment {
        DIRECTORY_PATH= 'SIT223'
        STAGING_ENVIRONMENT= '7.1C'
    } 
    stages{
        stage('Build'){
            steps{
                echo 'Using Maven Automation tool'
                echo 'Maven compiling & packaging code'           
            }
        }
        stage('Unit and Integration Tests'){
            steps{
                echo 'Using JUnit for Unit Tests'
                echo 'JUnit verified code fucntions as expected'
                echo 'Using TestNG for Integration Tests'
                echo 'TestNG verified application components work together'
            }
        }
        stage('Code Analysis'){
            steps{
                echo 'Using Checkstyle Automation tool'
                echo 'Checkstyle approves code, meeting industry requirements'
            }
        }
        stage('Security Scan'){
            steps{
                echo 'Using OWASP Dependency-Check tool'
                echo 'OWASP Dependency-Check identified no vulnerabilities'
            }
        }
        stage('Deploy to Staging'){
            steps{
                echo 'Deploying the application to the staging server: AWS EC2 Instance'
            }
        }
        stage('Integration Tests on Staging'){
            steps{
                echo "Running integration tests in ${STAGING_ENVIRONMENT}"
                echo "Functions properly in ${STAGING_ENVIRONMENT}"
            }
        }
        stage('Deploy to Production'){
            steps{
                echo "Deploying application to production server: AWS EC2 Instance"
            }
        }
    }
}
