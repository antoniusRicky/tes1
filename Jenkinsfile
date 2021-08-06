pipeline {
    agent any
    stages {
        stage('git repo & clean') {
            steps {
              bat "rmdir  /s /q TicketBookingServiceJunitTesting"
                bat "git clone https://github.com/antoniusRicky/tes1.git"
                bat "mvn clean -f TicketBookingServiceJunitTesting"
            }
        }
        stage('install') {
            steps {
                bat "mvn install -f TicketBookingServiceJunitTesting"
            }
        }
        stage('test') {
            steps {
                bat "mvn test -f TicketBookingServiceJunitTesting"
            }
        }
        
    }
}
