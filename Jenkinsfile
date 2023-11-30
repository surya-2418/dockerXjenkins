pipeline{
    agent any
        stages{
            stage ( "clone" )
            {
                steps{
                    sh ' git clone https://github.com/surya-2418/dockerXjenkins.git '
                }
            }
            stage ( "Build" )
            {
                steps{
                    sh ' docker build -t app  '
                }
            }
             stage ( "Run" )
            {
                steps{
                    sh ' docker run -it --name appPy  app '
                }
            }

        }
}
