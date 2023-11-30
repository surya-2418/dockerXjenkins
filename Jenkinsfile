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
                    
                    sh ' sudo docker build -f -t app . '
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
