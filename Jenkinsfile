pipeline 
{
			
	agent any

	stages 
	{
		stage('Clone') 
        {
            steps 
            {
               sh 'docker container prune -f'
               sh 'docker volume prune -f' 
               sh 'docker build -t app_build:latest . -f ./docker_clone'
               sh "docker run --name clone --rm --mount source=in,target=/volume_in git:latest"
               
            }
        }


        stage('Build') 
        {
            steps 
            {
               sh 'docker container prune -f'
               sh 'docker volume prune -f' 
               sh 'docker volume  create --name input_vol'
               sh 'docker volume  create --name out_vol'
               sh 'docker build -t app_build:latest . -f ./docker_build'
               sh 'docker run -v input_vol:/Cytoscape app_build'
               
            }
        }
		
	}
}
