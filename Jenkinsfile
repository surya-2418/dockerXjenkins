pipeline{
    agent any{
        stages{
            stage ( "clone" )
            {
                steps{
                    sh ' sudo git clone https://github.com/surya-2418/dockerXjenkins.git '
                }
            }
            stages ( "Build" )
            {
                steps{
                    sh ' sudo docker build -t app  '
                }
            }
             stages ( "Run" )
            {
                steps{
                    sh ' sudo docker run -it --name appPy  app '
                }
            }

        }
    }
}
