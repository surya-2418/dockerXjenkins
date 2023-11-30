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
                    
                    sh ' sudo docker build -t app /var/lib/jenkins/workspace/demo/dockerXjenkins '
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
