pipeline {
    environment {
        registry = "planetacomputer/app-jenkins1"
        registryCredential = 'dockerhub'
    }
    agent any
    stages { 
        stage('Push') { 
            steps { 
                 withCredentials([usernamePassword(credentialsId: 'dockerhub', passwordVariable: 'password', usernameVariable: 'user')]) {
                    sh 'docker login -u $user -p $password'
                    sh 'docker push planetacomputer/app-jenkins1'
                 }
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
                echo 'Fallo' // Ejecuta si fallas
                }
        }
}
