pipeline 
{
    agent any

    stages 
    {
        stage('Build') 
        {
            steps 
            {
                echo 'Build App in dev'
            }
        }

        stage('Test') 
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
                echo 'Deploy App in prod'
            }
        }
    }

    post
    {

    	always
    	{
    		emailext body: 'Summary', subject: 'Pipeline Status', to: 'anilkumbala@gmail.com'
    	}

    }
}
