pipeline{
    agent any
        stages{
            stage ( "clone" )
            {
                steps{
                    sh 'rm -rf * '
                    sh ' git clone https://github.com/surya-2418/dockerXjenkins.git '
                }
            }
            stage ( "Build" )
            {
                steps{
                    sudo sh ' sudo mv /var/lib/jenkins/workspace/demo/dockerXjenkins* /home/ec2-user/docker '
                    sh ' sudo docker build -t app . '
                }
            }
             stage ( "Run" )
            {
                steps{
                    sh ' sudo docker run -it --name appPy  app '
                }
            }

        }
}
