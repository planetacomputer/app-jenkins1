pipeline {
    agent any
    stages { 
        stage('Push') { 
            steps { 
                sh 'docker push czubeldia/app-jenkins1' 
            }  
        } 
    } 
        post {  
            always { 
                echo 'Siempre' // Ejecuta siempre
                }
            success {
                echo 'Todo Bien' // Ejecuta si todo bien
                }
            unstable {
                echo 'Inestable' // Ejecuta si inestable
                }
            failure { 
                echo 'Fallo' // Ejecuta si falla
                }
        }
}
