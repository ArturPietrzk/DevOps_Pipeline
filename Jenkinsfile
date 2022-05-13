pipeline 
{
			
	agent any

	stages 
	{
		stage('Clone') 
        {
            steps 
            {
              echo 'Clone'
               git branch: 'main', credentialsId: '6977c098-3192-4933-9512-ab1b9abc2433', url: 'https://github.com/ArturPietrzk/DevOps_Pipeline.git'
            }
        }


        stage('Build') 
        {
            steps 
            {
           	echo 'build'
               
            }
        }
		
	}
}
