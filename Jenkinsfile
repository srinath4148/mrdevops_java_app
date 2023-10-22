
pipeline{

    agent any

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
         
         when { expression {  params.action == 'create' } }

            steps{
               script{          
                   mvnTest()
               }
            }
        }
     
    }
}
