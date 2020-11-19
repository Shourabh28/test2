pipeline {
    agent any

    stages {

        stage ('creating the prop file') {
            steps {
                sh """
                  echo "name='shourabh'" > "test.properties"
                  echo "place='delhi'" >> "test.properties"
                  echo "country='india'" >> "test.properties"
                  echo "Hello everyone"
                """
            }
        }

        stage ('prepare') {
            steps {
                  script {
                      //loadProperties()
                      //def properties = readProperties file: 'test.properties'
                      load 'test.properties'
                      echo "${name}"
                  }
            }
        }

        stage ('Checking variables') {
            steps {
                  script {
                      echo "${name}"
                  }
            }
        }
        stage ('prepare') {
            steps {
                  script {
                      //loadProperties()
                      //def properties = 
                      properties = readProperties(file: 'test.properties')
                      echo "===========${properties}"
                      echo "Later one ${properties.name}"
                  }
            }
        }

        stage ('Checking variables') {
            steps {
                  script {
                      echo "Later one ${properties.place}"
                  }
            }
        }
    }
 }
