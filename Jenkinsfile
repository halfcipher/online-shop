node{

    stage('SCM Checkout')
    {
        git credentialsId: '926d3396-8af7-4568-b3b8-727bac660a19	', url: 'https://github.com/halfcipher/online-shop'
    }
    
    stage('Run Docker Compose File')
    {
        sh 'sudo docker-compose build'
        sh 'sudo docker-compose up -d'
    }
  stage('PUSH image to Docker Hub')
    {
      /* withCredentials([string(credentialsId: 'DockerHubPassword', variable: 'DHPWD')]) 
        {
            sh "docker login -u shubs3497 -p ${DHPWD}"
        }
        sh 'docker push vardhanns/phpmysql_app'
        */
        //docker.withRegistry( 'https://registry.hub.docker.com', 'DockerHubPassword' ) {
             
             sh 'sudo docker login -u "shubs3497" -p "AgB$$883" docker.io'
             //sh 'sudo docker push upasanatestdocker/mysql'
             //sh 'sudo docker push upasanatestdocker/job1_web1.0'
             sh 'sudo docker push shubs3497/job1_web2.0'
            // sh 'docker push upasanatestdocker/mysql'
          
    }
}
