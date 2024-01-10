pipeline 
{
    agent any

    stages 
    {
        stage('Artifact Registry Creation')
             
        {
            steps 
            {
                    echo 'Artifact Registry Creation'
                    sh 'terraform --version'
                    sh 'terraform init '
                    sh 'terraform plan '
                    //sh 'terraform apply -auto-approve'
                    
                
            }
        }

        stage('docker image Creation ') 
        {
            steps 
            {
                echo 'Test App in dev'
            }
        }

        stage('Deploy') 
        {
            steps 
            {
                echo 'Deploy App in production'
            }
        }
    }

    post
    {

    	always
    	{
    		cleanWs()
    	}

    }
}
