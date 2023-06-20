pipeline{
    agent any
    stages{
        stage('Build - construccion'){
            //Agregar comandos para construir la aplicacion
            steps {
                sh 'echo "etapa de construccion - done!"'
            }
        }
        stage('Test1 - primer set de pruebas'){
            parallel{
               stage('Pruebas Unitarias'){
                    steps {
                         sh 'sleep 5s'   
                         sh 'echo "Running unit test"'
                         //Agregar comandos para correr pruebas unitarias    
                    }
               }
                stage('Pruebas de integracion'){
                     steps{
                        sh 'echo "Running integration tests"'
                     }   
                }  
            } 
        }
        stage('Test2 - pruebas e2e'){
            parallel{
                stage('chrome'){
                    steps{
                        sh 'sleep 5s'
                        sh 'echo "Corriendo pruebas en Chrome"'
                    }
                }
                stage('safari'){
                    steps{
                        sh 'sleep 5s'
                        sh 'echo "Corriendo pruebas en Safari"'
                    }
                }
                stage('edge'){
                    steps{
                        sh 'sleep 5s'
                        sh 'echo "Corriendo pruebas en Edge"'
                    }
                }
            }    
        }
        stage('Deploy'){
            steps{
                sh 'echo "Entregando la aplicacion"'
                //agregamos los comandos para entregar la aplicacion
            }
        }
    }
}
