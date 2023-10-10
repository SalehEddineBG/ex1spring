pipeline {
    agent any 
    tools { 
        maven 'maven'
    }
    stages {
        stage ("Clean up"){
            
            steps {
                deleteDir()
            }
        }
        stage ("Clone repo"){
            steps {
                sh "git clone https://github.com/SalehEddineBG/ex1spring"
            }
        }
        stage ("Generate backend image") {
              steps {
                   dir("ex1spring"){
                      sh "mvn clean install"
                      sh "docker build -t docexp1-spring ."
                  }                
              }
          }
        stage ("Run docker compose") {
            steps {
                 dir("exp1spring"){
                    sh "docker compose up -d"
                }                
            }
        }
    }
}
        stage ("Run docker compose") {
            steps {
                 dir("exp1-spring"){
                    sh " docker compose up -d"
                }                
            }
        }
    }
}
