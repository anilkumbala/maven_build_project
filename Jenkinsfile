pipeline 
{
    agent any

    environment {
        GOOGLE_APPLICATION_CREDENTIALS = credentials('anilgcpcredentials')
    }

    stages 
    {
        stage('Artifact Registry Creation')
             
        {
            steps 
            {
                // Set up Google Cloud SDK
                    sh 'gcloud auth activate-service-account --key-file=$GOOGLE_APPLICATION_CREDENTIALS'
                    sh 'gcloud config set project excellent-guide-410011'
                    echo 'Artifact Registry Creation'
                    sh 'terraform --version'
                    sh 'terraform init '
                    sh 'terraform plan '
                    sh 'terraform apply -auto-approve'
                    
                
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
