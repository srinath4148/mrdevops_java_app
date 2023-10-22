@Library('my-shared-library') _
pipeline{

    agent any
    parameters{

        choice(name: 'action', choices: 'create\ndelete', description: 'Choose create/Destroy')
    }
    stages{
         
        stage('Git Checkout'){
            steps{
            gitCheckout(
                branch: "main",
                url: "https://github.com/srinath4148/mrdevops_java_app.git"
            )
            }
        }
         stage('Unit Test maven'){       

            steps{
               script{          
                   mvnTest()
               }
            }
        }
        stage('Integration Test maven'){       

            steps{
               script{          
                   mvnIntegrationTest()
               }
            }
        }
    }
}
